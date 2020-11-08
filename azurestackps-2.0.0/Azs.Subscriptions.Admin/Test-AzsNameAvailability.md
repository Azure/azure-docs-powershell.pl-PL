---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054064"
---
# <span data-ttu-id="3fe9d-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="3fe9d-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="3fe9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fe9d-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe9d-103">Zapoznaj się z listą abonamentów.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="3fe9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fe9d-104">SYNTAX</span></span>

### <span data-ttu-id="3fe9d-105">CheckExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3fe9d-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3fe9d-106">Wyszukaj</span><span class="sxs-lookup"><span data-stu-id="3fe9d-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3fe9d-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3fe9d-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3fe9d-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3fe9d-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3fe9d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3fe9d-109">DESCRIPTION</span></span>
<span data-ttu-id="3fe9d-110">Zapoznaj się z listą abonamentów.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="3fe9d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fe9d-111">EXAMPLES</span></span>

### <span data-ttu-id="3fe9d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3fe9d-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="3fe9d-113">Zwraca dostępność określonego typu i nazwy zasobu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="3fe9d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fe9d-114">PARAMETERS</span></span>

### <span data-ttu-id="3fe9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe9d-115">-DefaultProfile</span></span>
<span data-ttu-id="3fe9d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fe9d-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3fe9d-117">-InputObject</span></span>
<span data-ttu-id="3fe9d-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3fe9d-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3fe9d-119">-Name</span></span>
<span data-ttu-id="3fe9d-120">Nazwa zasobu do zweryfikowania.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-120">The resource name to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3fe9d-121">-NameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="3fe9d-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="3fe9d-122">Definicja akcji Sprawdź dostępność nazw.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-122">The check name availability action definition.</span></span>
<span data-ttu-id="3fe9d-123">Aby skonstruować, zobacz sekcję notatki dla właściwości NAMEAVAILABILITYDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3fe9d-124">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3fe9d-124">-ResourceType</span></span>
<span data-ttu-id="3fe9d-125">Typ zasobu do zweryfikowania.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-125">The resource type to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3fe9d-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3fe9d-126">-SubscriptionId</span></span>
<span data-ttu-id="3fe9d-127">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3fe9d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3fe9d-128">-Confirm</span></span>
<span data-ttu-id="3fe9d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fe9d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fe9d-130">-WhatIf</span></span>
<span data-ttu-id="3fe9d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fe9d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fe9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe9d-133">CommonParameters</span></span>
<span data-ttu-id="3fe9d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe9d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fe9d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe9d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fe9d-136">INPUTS</span></span>

### <span data-ttu-id="3fe9d-137">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. ICheckNameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="3fe9d-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="3fe9d-138">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3fe9d-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="3fe9d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fe9d-139">OUTPUTS</span></span>

### <span data-ttu-id="3fe9d-140">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. ICheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3fe9d-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="3fe9d-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3fe9d-141">ALIASES</span></span>

## <span data-ttu-id="3fe9d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fe9d-142">NOTES</span></span>

<span data-ttu-id="3fe9d-143">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3fe9d-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3fe9d-145">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3fe9d-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3fe9d-146">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="3fe9d-147">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="3fe9d-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3fe9d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3fe9d-149">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="3fe9d-150">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="3fe9d-151">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="3fe9d-152">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="3fe9d-153">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="3fe9d-154">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="3fe9d-155">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="3fe9d-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="3fe9d-156">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3fe9d-157">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="3fe9d-158">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3fe9d-159">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="3fe9d-160">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="3fe9d-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition> : sprawdzenie definicji akcji dostępność nazw.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="3fe9d-162">`[Name <String>]`: Nazwa zasobu do zweryfikowania.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="3fe9d-163">`[ResourceType <String>]`: Typ zasobu do sprawdzenia.</span><span class="sxs-lookup"><span data-stu-id="3fe9d-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="3fe9d-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fe9d-164">RELATED LINKS</span></span>

