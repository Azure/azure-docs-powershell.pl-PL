---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054067"
---
# <span data-ttu-id="e8f51-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="e8f51-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="e8f51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8f51-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f51-103">Tworzy lub aktualizuje określoną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="e8f51-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="e8f51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8f51-104">SYNTAX</span></span>

### <span data-ttu-id="e8f51-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8f51-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e8f51-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="e8f51-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e8f51-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e8f51-107">DESCRIPTION</span></span>
<span data-ttu-id="e8f51-108">Tworzy lub aktualizuje określoną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="e8f51-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="e8f51-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8f51-109">EXAMPLES</span></span>

### <span data-ttu-id="e8f51-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8f51-110">Example 1</span></span>
```powershell
PS C:\> $Subscription = Get-AzsUserSubscription | Select-Object -First 1
$Subscription.DisplayName = 'Update User Subscription'
$Subscription | Set-AzsUserSubscription | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : Update User Subscription
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="e8f51-111">Aktualizuje subskrypcję</span><span class="sxs-lookup"><span data-stu-id="e8f51-111">Updates a subscription</span></span>

## <span data-ttu-id="e8f51-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8f51-112">PARAMETERS</span></span>

### <span data-ttu-id="e8f51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f51-113">-DefaultProfile</span></span>
<span data-ttu-id="e8f51-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f51-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f51-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8f51-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="e8f51-116">Identyfikator subskrypcji DelegatedProvider nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="e8f51-116">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="e8f51-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e8f51-117">-DisplayName</span></span>
<span data-ttu-id="e8f51-118">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8f51-118">Subscription name.</span></span>

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

### <span data-ttu-id="e8f51-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="e8f51-119">-ExternalReferenceId</span></span>
<span data-ttu-id="e8f51-120">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="e8f51-120">External reference identifier.</span></span>

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

### <span data-ttu-id="e8f51-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e8f51-121">-Id</span></span>
<span data-ttu-id="e8f51-122">W pełni kwalifikowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="e8f51-122">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="e8f51-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e8f51-123">-OfferId</span></span>
<span data-ttu-id="e8f51-124">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="e8f51-124">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="e8f51-125">-Właściciel</span><span class="sxs-lookup"><span data-stu-id="e8f51-125">-Owner</span></span>
<span data-ttu-id="e8f51-126">Właściciel subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8f51-126">Subscription owner.</span></span>

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

### <span data-ttu-id="e8f51-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="e8f51-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="e8f51-128">Typ Menedżera zasobów routingu.</span><span class="sxs-lookup"><span data-stu-id="e8f51-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e8f51-129">-State</span><span class="sxs-lookup"><span data-stu-id="e8f51-129">-State</span></span>
<span data-ttu-id="e8f51-130">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e8f51-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e8f51-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="e8f51-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="e8f51-132">Właściwości obiektu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8f51-132">Subscription object properties.</span></span>
<span data-ttu-id="e8f51-133">Aby skonstruować, zobacz sekcję notatki dla właściwości SUBSCRIPTIONDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="e8f51-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e8f51-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e8f51-134">-SubscriptionId</span></span>
<span data-ttu-id="e8f51-135">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="e8f51-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e8f51-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="e8f51-136">-SubscriptionId1</span></span>
<span data-ttu-id="e8f51-137">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8f51-137">Subscription identifier.</span></span>

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

### <span data-ttu-id="e8f51-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8f51-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="e8f51-139">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e8f51-139">The target subscription ID.</span></span>

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

### <span data-ttu-id="e8f51-140">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e8f51-140">-TenantId</span></span>
<span data-ttu-id="e8f51-141">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="e8f51-141">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="e8f51-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8f51-142">-Confirm</span></span>
<span data-ttu-id="e8f51-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8f51-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f51-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f51-144">-WhatIf</span></span>
<span data-ttu-id="e8f51-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8f51-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8f51-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8f51-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f51-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f51-147">CommonParameters</span></span>
<span data-ttu-id="e8f51-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8f51-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f51-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8f51-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f51-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8f51-150">INPUTS</span></span>

### <span data-ttu-id="e8f51-151">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="e8f51-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="e8f51-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8f51-152">OUTPUTS</span></span>

### <span data-ttu-id="e8f51-153">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="e8f51-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="e8f51-154">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e8f51-154">ALIASES</span></span>

## <span data-ttu-id="e8f51-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8f51-155">NOTES</span></span>

<span data-ttu-id="e8f51-156">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e8f51-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e8f51-157">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e8f51-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e8f51-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : właściwości obiektu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8f51-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="e8f51-159">`[DelegatedProviderSubscriptionId <String>]`: Nadrzędny Identyfikator subskrypcji DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="e8f51-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="e8f51-160">`[DisplayName <String>]`: Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8f51-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="e8f51-161">`[ExternalReferenceId <String>]`: Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="e8f51-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="e8f51-162">`[Id <String>]`: W pełni kwalifikowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="e8f51-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="e8f51-163">`[OfferId <String>]`: Identyfikator oferty w zakresie dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="e8f51-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="e8f51-164">`[Owner <String>]`: Właściciel subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8f51-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="e8f51-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Typ Menedżera zasobów routingu.</span><span class="sxs-lookup"><span data-stu-id="e8f51-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="e8f51-166">`[State <SubscriptionState?>]`: Stan subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8f51-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="e8f51-167">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8f51-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="e8f51-168">`[TenantId <String>]`: Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="e8f51-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="e8f51-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8f51-169">RELATED LINKS</span></span>

