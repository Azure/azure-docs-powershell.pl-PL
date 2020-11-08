---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsoffer
schema: 2.0.0
ms.openlocfilehash: 82be26ae402278d8cdc24195fd62ed09b67bdc14
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054074"
---
# <span data-ttu-id="e10fb-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="e10fb-101">Set-AzsOffer</span></span>

## <span data-ttu-id="e10fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e10fb-102">SYNOPSIS</span></span>
<span data-ttu-id="e10fb-103">Utwórz lub zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="e10fb-103">Create or update the offer.</span></span>

## <span data-ttu-id="e10fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e10fb-104">SYNTAX</span></span>

### <span data-ttu-id="e10fb-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e10fb-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-BasePlanIds <String[]>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-MaxSubscriptionsPerAccount <Int32>] [-PropertiesName <String>] [-State <AccessibilityState>]
 [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e10fb-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="e10fb-106">Update</span></span>
```
Set-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e10fb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e10fb-107">DESCRIPTION</span></span>
<span data-ttu-id="e10fb-108">Utwórz lub zaktualizuj ofertę.</span><span class="sxs-lookup"><span data-stu-id="e10fb-108">Create or update the offer.</span></span>

## <span data-ttu-id="e10fb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e10fb-109">EXAMPLES</span></span>

### <span data-ttu-id="e10fb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e10fb-110">Example 1</span></span>
```powershell
PS C:\> $Offer = Get-AzsAdminManagedOffer | Select-Object -First 1
$Offer.MaxSubscriptionsPerAccount = 18
$Offer | Set-AzsOffer

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056}
Description                : 
DisplayName                : DRPTestOffer5056
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Location                   : redmond
MaxSubscriptionsPerAccount : 18
Name                       : DRPTestOffer5056
PropertiesName             : DRPTestOffer5056
State                      : Private
SubscriptionCount          : 5
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="e10fb-111">Aktualizowanie oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-111">Update an offer.</span></span>

## <span data-ttu-id="e10fb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e10fb-112">PARAMETERS</span></span>

### <span data-ttu-id="e10fb-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="e10fb-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="e10fb-114">Odwołania do planów dodatków, które dzierżawa mogą opcjonalnie nabyć jako część oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="e10fb-115">Aby skonstruować, zobacz sekcję notatki dla właściwości ADDONPLANDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="e10fb-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="e10fb-116">-BasePlanIds</span></span>
<span data-ttu-id="e10fb-117">Identyfikatory planów podstawowych, które są dostępne dla dzierżawy natychmiast po zasubskrybowaniu oferty przez dzierżawcę.</span><span class="sxs-lookup"><span data-stu-id="e10fb-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10fb-118">-DefaultProfile</span></span>
<span data-ttu-id="e10fb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e10fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e10fb-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="e10fb-120">-Description</span></span>
<span data-ttu-id="e10fb-121">Opis oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-121">Description of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e10fb-122">-DisplayName</span></span>
<span data-ttu-id="e10fb-123">Nazwa wyświetlana oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-123">Display name of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="e10fb-124">-ExternalReferenceId</span></span>
<span data-ttu-id="e10fb-125">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="e10fb-125">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e10fb-126">-Location</span></span>
<span data-ttu-id="e10fb-127">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="e10fb-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="e10fb-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="e10fb-129">Maksymalna liczba abonamentów na konto.</span><span class="sxs-lookup"><span data-stu-id="e10fb-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e10fb-130">-Name</span></span>
<span data-ttu-id="e10fb-131">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-131">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="e10fb-132">-OfferDefinition</span></span>
<span data-ttu-id="e10fb-133">Przedstawia oferowanie usług, za które można utworzyć abonament.</span><span class="sxs-lookup"><span data-stu-id="e10fb-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="e10fb-134">Aby skonstruować, zobacz sekcję notatki dla właściwości OFFERDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="e10fb-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-135">-Propertiesname</span><span class="sxs-lookup"><span data-stu-id="e10fb-135">-PropertiesName</span></span>
<span data-ttu-id="e10fb-136">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-136">Name of the Offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e10fb-137">-ResourceGroupName</span></span>
<span data-ttu-id="e10fb-138">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="e10fb-138">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-139">-State</span><span class="sxs-lookup"><span data-stu-id="e10fb-139">-State</span></span>
<span data-ttu-id="e10fb-140">Stan ułatwień dostępu w ofercie.</span><span class="sxs-lookup"><span data-stu-id="e10fb-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="e10fb-141">-SubscriptionCount</span></span>
<span data-ttu-id="e10fb-142">Bieżąca liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="e10fb-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e10fb-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e10fb-143">-SubscriptionId</span></span>
<span data-ttu-id="e10fb-144">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="e10fb-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e10fb-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e10fb-145">-Confirm</span></span>
<span data-ttu-id="e10fb-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e10fb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e10fb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e10fb-147">-WhatIf</span></span>
<span data-ttu-id="e10fb-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e10fb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e10fb-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e10fb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e10fb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10fb-150">CommonParameters</span></span>
<span data-ttu-id="e10fb-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e10fb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10fb-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e10fb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10fb-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e10fb-153">INPUTS</span></span>

### <span data-ttu-id="e10fb-154">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="e10fb-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="e10fb-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e10fb-155">OUTPUTS</span></span>

### <span data-ttu-id="e10fb-156">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="e10fb-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="e10fb-157">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e10fb-157">ALIASES</span></span>

## <span data-ttu-id="e10fb-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e10fb-158">NOTES</span></span>

<span data-ttu-id="e10fb-159">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e10fb-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e10fb-160">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e10fb-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e10fb-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >: odwołania do planów dodatków, które dzierżawa mogą opcjonalnie nabyć jako część oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="e10fb-162">`[MaxAcquisitionCount <Int32?>]`: Maksymalna liczba wystąpień, które można nabyć w ramach pojedynczego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e10fb-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="e10fb-163">Jeśli argument nie zostanie określony, przyjmowana jest wartość 1.</span><span class="sxs-lookup"><span data-stu-id="e10fb-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="e10fb-164">`[PlanId <String>]`: Identyfikator planu.</span><span class="sxs-lookup"><span data-stu-id="e10fb-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="e10fb-165">OFFERDEFINITION <IOffer> : przedstawia oferowanie usług, za które można utworzyć abonament.</span><span class="sxs-lookup"><span data-stu-id="e10fb-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="e10fb-166">`[Location <String>]`: Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="e10fb-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="e10fb-167">`[AddonPlans <IAddonPlanDefinition[]>]`: Odwołania do planów dodatków, które dzierżawa mogą opcjonalnie nabyć jako część oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="e10fb-168">`[MaxAcquisitionCount <Int32?>]`: Maksymalna liczba wystąpień, które można nabyć w ramach pojedynczego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e10fb-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="e10fb-169">Jeśli argument nie zostanie określony, przyjmowana jest wartość 1.</span><span class="sxs-lookup"><span data-stu-id="e10fb-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="e10fb-170">`[PlanId <String>]`: Identyfikator planu.</span><span class="sxs-lookup"><span data-stu-id="e10fb-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="e10fb-171">`[BasePlanIds <String[]>]`: Identyfikatory planów podstawowych, które są dostępne dla dzierżawy natychmiast po zasubskrybowaniu oferty przez dzierżawcę.</span><span class="sxs-lookup"><span data-stu-id="e10fb-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="e10fb-172">`[Description <String>]`: Opis oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="e10fb-173">`[DisplayName <String>]`: Wyświetlana nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="e10fb-174">`[ExternalReferenceId <String>]`: Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="e10fb-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="e10fb-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maksymalna liczba abonamentów na konto.</span><span class="sxs-lookup"><span data-stu-id="e10fb-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="e10fb-176">`[PropertiesName <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="e10fb-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="e10fb-177">`[State <AccessibilityState?>]`: Stan ułatwień dostępu oferowanie.</span><span class="sxs-lookup"><span data-stu-id="e10fb-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="e10fb-178">`[SubscriptionCount <Int32?>]`: Liczba bieżących abonamentów.</span><span class="sxs-lookup"><span data-stu-id="e10fb-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="e10fb-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e10fb-179">RELATED LINKS</span></span>

