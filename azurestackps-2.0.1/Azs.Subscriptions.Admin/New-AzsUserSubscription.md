---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054145"
---
# <span data-ttu-id="d94de-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="d94de-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="d94de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d94de-102">SYNOPSIS</span></span>
<span data-ttu-id="d94de-103">Tworzy lub aktualizuje określoną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="d94de-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="d94de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d94de-104">SYNTAX</span></span>

### <span data-ttu-id="d94de-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d94de-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d94de-106">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="d94de-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d94de-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d94de-107">DESCRIPTION</span></span>
<span data-ttu-id="d94de-108">Tworzy lub aktualizuje określoną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="d94de-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="d94de-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d94de-109">EXAMPLES</span></span>

### <span data-ttu-id="d94de-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d94de-110">Example 1</span></span>
```powershell
PS C:\> New-AzsUserSubscription -Owner "user@contoso.com" -OfferId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOffer" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : 
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/398466a8-7d43-455a-b842-772d356d119e
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOff
                                  er
Owner                           : user@contoso.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : 398466a8-7d43-455a-b842-772d356d119e
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="d94de-111">Tworzy nową subskrypcję użytkownika</span><span class="sxs-lookup"><span data-stu-id="d94de-111">Creates a new user subscription</span></span>

## <span data-ttu-id="d94de-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d94de-112">PARAMETERS</span></span>

### <span data-ttu-id="d94de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94de-113">-DefaultProfile</span></span>
<span data-ttu-id="d94de-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d94de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d94de-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d94de-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="d94de-116">Identyfikator subskrypcji DelegatedProvider nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="d94de-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d94de-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d94de-117">-DisplayName</span></span>
<span data-ttu-id="d94de-118">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d94de-118">Subscription name.</span></span>

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

### <span data-ttu-id="d94de-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="d94de-119">-ExternalReferenceId</span></span>
<span data-ttu-id="d94de-120">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="d94de-120">External reference identifier.</span></span>

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

### <span data-ttu-id="d94de-121">-ID</span><span class="sxs-lookup"><span data-stu-id="d94de-121">-Id</span></span>
<span data-ttu-id="d94de-122">W pełni kwalifikowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="d94de-122">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="d94de-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="d94de-123">-OfferId</span></span>
<span data-ttu-id="d94de-124">Identyfikator oferty w ramach zakresu dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="d94de-124">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="d94de-125">-Właściciel</span><span class="sxs-lookup"><span data-stu-id="d94de-125">-Owner</span></span>
<span data-ttu-id="d94de-126">Właściciel subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d94de-126">Subscription owner.</span></span>

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

### <span data-ttu-id="d94de-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="d94de-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="d94de-128">Typ Menedżera zasobów routingu.</span><span class="sxs-lookup"><span data-stu-id="d94de-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Default"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d94de-129">-State</span><span class="sxs-lookup"><span data-stu-id="d94de-129">-State</span></span>
<span data-ttu-id="d94de-130">Stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="d94de-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d94de-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="d94de-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="d94de-132">Właściwości obiektu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d94de-132">Subscription object properties.</span></span>
<span data-ttu-id="d94de-133">Aby skonstruować, zobacz sekcję notatki dla właściwości SUBSCRIPTIONDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="d94de-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d94de-134">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d94de-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="d94de-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="d94de-135">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d94de-136">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="d94de-136">-TenantId</span></span>
<span data-ttu-id="d94de-137">Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="d94de-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="d94de-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d94de-138">-Confirm</span></span>
<span data-ttu-id="d94de-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d94de-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d94de-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d94de-140">-WhatIf</span></span>
<span data-ttu-id="d94de-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d94de-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d94de-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d94de-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d94de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94de-143">CommonParameters</span></span>
<span data-ttu-id="d94de-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d94de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94de-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d94de-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94de-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d94de-146">INPUTS</span></span>

### <span data-ttu-id="d94de-147">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="d94de-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="d94de-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d94de-148">OUTPUTS</span></span>

### <span data-ttu-id="d94de-149">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="d94de-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="d94de-150">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d94de-150">ALIASES</span></span>

## <span data-ttu-id="d94de-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d94de-151">NOTES</span></span>

<span data-ttu-id="d94de-152">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d94de-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d94de-153">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d94de-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d94de-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : właściwości obiektu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d94de-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="d94de-155">`[DelegatedProviderSubscriptionId <String>]`: Nadrzędny Identyfikator subskrypcji DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="d94de-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="d94de-156">`[DisplayName <String>]`: Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d94de-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="d94de-157">`[ExternalReferenceId <String>]`: Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="d94de-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="d94de-158">`[Id <String>]`: W pełni kwalifikowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="d94de-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="d94de-159">`[OfferId <String>]`: Identyfikator oferty w zakresie dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="d94de-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="d94de-160">`[Owner <String>]`: Właściciel subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d94de-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="d94de-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Typ Menedżera zasobów routingu.</span><span class="sxs-lookup"><span data-stu-id="d94de-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="d94de-162">`[State <SubscriptionState?>]`: Stan subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d94de-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="d94de-163">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d94de-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="d94de-164">`[TenantId <String>]`: Identyfikator dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="d94de-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="d94de-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d94de-165">RELATED LINKS</span></span>

