---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054265"
---
# <span data-ttu-id="9842d-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="9842d-101">Close-AzsAlert</span></span>

## <span data-ttu-id="9842d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9842d-102">SYNOPSIS</span></span>
<span data-ttu-id="9842d-103">Zamyka dany alert.</span><span class="sxs-lookup"><span data-stu-id="9842d-103">Closes the given alert.</span></span>

## <span data-ttu-id="9842d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9842d-104">SYNTAX</span></span>

### <span data-ttu-id="9842d-105">CloseExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9842d-105">CloseExpanded (Default)</span></span>
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9842d-106">Zamknij</span><span class="sxs-lookup"><span data-stu-id="9842d-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9842d-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9842d-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9842d-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9842d-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9842d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9842d-109">DESCRIPTION</span></span>
<span data-ttu-id="9842d-110">Zamyka dany alert.</span><span class="sxs-lookup"><span data-stu-id="9842d-110">Closes the given alert.</span></span>

## <span data-ttu-id="9842d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9842d-111">EXAMPLES</span></span>

### <span data-ttu-id="9842d-112">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="9842d-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="9842d-113">Zamknij alert według nazwy.</span><span class="sxs-lookup"><span data-stu-id="9842d-113">Close an alert by Name.</span></span>

### <span data-ttu-id="9842d-114">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="9842d-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="9842d-115">Zamykanie alertu za pośrednictwem połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="9842d-115">Close an alert through piping.</span></span>

## <span data-ttu-id="9842d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9842d-116">PARAMETERS</span></span>

### <span data-ttu-id="9842d-117">-Alert</span><span class="sxs-lookup"><span data-stu-id="9842d-117">-Alert</span></span>
<span data-ttu-id="9842d-118">Ten obiekt reprezentuje zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-118">This object represents an alert resource.</span></span>
<span data-ttu-id="9842d-119">Aby skonstruować, zobacz sekcję notatki dla właściwości ALERTu i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="9842d-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="9842d-120">-AlertId</span></span>
<span data-ttu-id="9842d-121">Pobiera lub ustawia identyfikator alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-121">Gets or sets the ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="9842d-122">-AlertProperty</span></span>
<span data-ttu-id="9842d-123">Właściwości alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-123">Properties of the alert.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="9842d-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="9842d-125">Alias użytkownika, który zamknął alert.</span><span class="sxs-lookup"><span data-stu-id="9842d-125">User alias who closed the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="9842d-126">-ClosedTimestamp</span></span>
<span data-ttu-id="9842d-127">Sygnatura czasowa po zamknięciu alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-127">Timestamp when the alert was closed.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="9842d-128">-CreatedTimestamp</span></span>
<span data-ttu-id="9842d-129">Sygnatura czasowa utworzenia alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-129">Timestamp when the alert was created.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9842d-130">-DefaultProfile</span></span>
<span data-ttu-id="9842d-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9842d-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9842d-132">— Opis</span><span class="sxs-lookup"><span data-stu-id="9842d-132">-Description</span></span>
<span data-ttu-id="9842d-133">Opis alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-133">Description of the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="9842d-134">-FaultId</span></span>
<span data-ttu-id="9842d-135">Pobiera lub ustawia identyfikator błędu alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-135">Gets or sets the fault ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="9842d-136">-FaultTypeId</span></span>
<span data-ttu-id="9842d-137">Pobiera lub ustawia identyfikator typu błędu alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-137">Gets or sets the fault type ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="9842d-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="9842d-139">Wskazuje, czy można skorygować alert.</span><span class="sxs-lookup"><span data-stu-id="9842d-139">Indicates if the alert can be remediated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="9842d-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="9842d-141">Nazwa wyświetlana elementu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="9842d-141">Display name for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="9842d-142">-ImpactedResourceId</span></span>
<span data-ttu-id="9842d-143">Pobiera lub ustawia identyfikator zasobu dla elementu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="9842d-143">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-144">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9842d-144">-InputObject</span></span>
<span data-ttu-id="9842d-145">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9842d-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="9842d-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="9842d-147">Sygnatura czasowa ostatniej aktualizacji alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-147">Timestamp when the alert was last updated.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-148">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9842d-148">-Location</span></span>
<span data-ttu-id="9842d-149">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="9842d-149">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="9842d-150">-Location1</span></span>
<span data-ttu-id="9842d-151">Obszar platformy Azure, w którym znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="9842d-151">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-152">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9842d-152">-Name</span></span>
<span data-ttu-id="9842d-153">Nazwa alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-153">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-154">-Korygowanie</span><span class="sxs-lookup"><span data-stu-id="9842d-154">-Remediation</span></span>
<span data-ttu-id="9842d-155">Pobiera lub ustawia przyjazne dla administratora instrukcje dotyczące korygowania alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9842d-156">-ResourceGroupName</span></span>
<span data-ttu-id="9842d-157">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9842d-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="9842d-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="9842d-159">Pobiera lub ustawia identyfikator rejestracji usługi, do której należy alert.</span><span class="sxs-lookup"><span data-stu-id="9842d-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="9842d-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="9842d-161">Pobiera lub ustawia identyfikator rejestracji zasobu skojarzonego z alertem.</span><span class="sxs-lookup"><span data-stu-id="9842d-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="9842d-162">Jeśli alert nie jest skojarzony z zasobem, Identyfikator rejestracji zasobu ma wartość null.</span><span class="sxs-lookup"><span data-stu-id="9842d-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-163">— Ważność</span><span class="sxs-lookup"><span data-stu-id="9842d-163">-Severity</span></span>
<span data-ttu-id="9842d-164">Ważność alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-164">Severity of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-165">-State</span><span class="sxs-lookup"><span data-stu-id="9842d-165">-State</span></span>
<span data-ttu-id="9842d-166">Stan alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-166">State of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-167">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9842d-167">-SubscriptionId</span></span>
<span data-ttu-id="9842d-168">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9842d-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9842d-169">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="9842d-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="9842d-170">-Tag</span></span>
<span data-ttu-id="9842d-171">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="9842d-171">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-172">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="9842d-172">-Title</span></span>
<span data-ttu-id="9842d-173">Pobiera lub ustawia identyfikator zasobu dla elementu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="9842d-173">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-174">-User</span><span class="sxs-lookup"><span data-stu-id="9842d-174">-User</span></span>
<span data-ttu-id="9842d-175">Nazwa użytkownika używana do wykonania operacji.</span><span class="sxs-lookup"><span data-stu-id="9842d-175">The username used to perform the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9842d-176">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9842d-176">-Confirm</span></span>
<span data-ttu-id="9842d-177">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9842d-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9842d-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9842d-178">-WhatIf</span></span>
<span data-ttu-id="9842d-179">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9842d-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9842d-180">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9842d-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9842d-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9842d-181">CommonParameters</span></span>
<span data-ttu-id="9842d-182">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9842d-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9842d-183">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9842d-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9842d-184">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9842d-184">INPUTS</span></span>

### <span data-ttu-id="9842d-185">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="9842d-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="9842d-186">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9842d-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="9842d-187">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9842d-187">OUTPUTS</span></span>

### <span data-ttu-id="9842d-188">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="9842d-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="9842d-189">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9842d-189">NOTES</span></span>

<span data-ttu-id="9842d-190">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9842d-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9842d-191">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9842d-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9842d-192">ALERT <IAlert> : ten obiekt reprezentuje zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="9842d-193">`[Location <String>]`: Obszar platformy Azure, w którym mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="9842d-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="9842d-194">`[Tag <ITrackedResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="9842d-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="9842d-195">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="9842d-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="9842d-196">`[AlertId <String>]`: Pobiera lub ustawia identyfikator alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="9842d-197">`[AlertProperty <IAlertModelAlertProperties>]`: Właściwości alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="9842d-198">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="9842d-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="9842d-199">`[ClosedByUserAlias <String>]`: Alias użytkownika, który zamknął alert.</span><span class="sxs-lookup"><span data-stu-id="9842d-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="9842d-200">`[ClosedTimestamp <String>]`: Sygnatura czasowa, gdy alert został zamknięty.</span><span class="sxs-lookup"><span data-stu-id="9842d-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="9842d-201">`[CreatedTimestamp <String>]`: Sygnatura czasowa utworzenia alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="9842d-202">`[Description <IDictionary[]>]`: Opis alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="9842d-203">`[FaultId <String>]`: Pobiera lub ustawia identyfikator błędu alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="9842d-204">`[FaultTypeId <String>]`: Pobiera lub ustawia identyfikator typu błędu alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="9842d-205">`[HasValidRemediationAction <Boolean?>]`: Wskazuje, czy można skorygować alert.</span><span class="sxs-lookup"><span data-stu-id="9842d-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="9842d-206">`[ImpactedResourceDisplayName <String>]`: Wyświetlana nazwa elementu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="9842d-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="9842d-207">`[ImpactedResourceId <String>]`: Pobiera lub ustawia identyfikator zasobu dla elementu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="9842d-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="9842d-208">`[LastUpdatedTimestamp <String>]`: Sygnatura czasowa ostatniej aktualizacji alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="9842d-209">`[Remediation <IDictionary[]>]`: Pobiera lub ustawia przyjazne instrukcje dotyczące korygowania administratora dla alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="9842d-210">`[ResourceProviderRegistrationId <String>]`: Pobiera lub ustawia identyfikator rejestracji usługi, do której należy alert.</span><span class="sxs-lookup"><span data-stu-id="9842d-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="9842d-211">`[ResourceRegistrationId <String>]`: Pobiera lub ustawia identyfikator rejestracji zasobu skojarzonego z alertem.</span><span class="sxs-lookup"><span data-stu-id="9842d-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="9842d-212">Jeśli alert nie jest skojarzony z zasobem, Identyfikator rejestracji zasobu ma wartość null.</span><span class="sxs-lookup"><span data-stu-id="9842d-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="9842d-213">`[Severity <String>]`: Dotkliwość alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="9842d-214">`[State <String>]`: Stan alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="9842d-215">`[Title <String>]`: Pobiera lub ustawia identyfikator zasobu dla elementu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="9842d-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="9842d-216">INPUTobject <IInfrastructureInsightsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="9842d-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9842d-217">`[AlertName <String>]`: Nazwa alertu.</span><span class="sxs-lookup"><span data-stu-id="9842d-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="9842d-218">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9842d-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9842d-219">`[Location <String>]`: Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="9842d-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="9842d-220">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9842d-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9842d-221">`[ResourceRegistrationId <String>]`: Identyfikator rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="9842d-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="9842d-222">`[ServiceHealth <String>]`: Nazwa kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="9842d-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="9842d-223">`[ServiceRegistrationId <String>]`: Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="9842d-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="9842d-224">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9842d-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9842d-225">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="9842d-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9842d-226">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9842d-226">RELATED LINKS</span></span>

