---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/add-azsplantooffer
schema: 2.0.0
ms.openlocfilehash: 65691116ea8e73e8f03e8cc7dc97f38c61ecebdb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054206"
---
# <span data-ttu-id="0eae7-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="0eae7-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="0eae7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0eae7-102">SYNOPSIS</span></span>
<span data-ttu-id="0eae7-103">Łączy plan z ofertą.</span><span class="sxs-lookup"><span data-stu-id="0eae7-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="0eae7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0eae7-104">SYNTAX</span></span>

### <span data-ttu-id="0eae7-105">LinkExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0eae7-105">LinkExpanded (Default)</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0eae7-106">Łącze</span><span class="sxs-lookup"><span data-stu-id="0eae7-106">Link</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0eae7-107">LinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0eae7-107">LinkViaIdentity</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0eae7-108">LinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0eae7-108">LinkViaIdentityExpanded</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0eae7-109">Opis</span><span class="sxs-lookup"><span data-stu-id="0eae7-109">DESCRIPTION</span></span>
<span data-ttu-id="0eae7-110">Łączy plan z ofertą.</span><span class="sxs-lookup"><span data-stu-id="0eae7-110">Links a plan to an offer.</span></span>

## <span data-ttu-id="0eae7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0eae7-111">EXAMPLES</span></span>

### <span data-ttu-id="0eae7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0eae7-112">Example 1</span></span>
```powershell
PS C:\> Add-AzsPlanToOffer -PlanName "addonplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg" -MaxAcquisitionCount 18

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
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

<span data-ttu-id="0eae7-113">Łączy plan z ofertą.</span><span class="sxs-lookup"><span data-stu-id="0eae7-113">Links a plan to an offer.</span></span>

## <span data-ttu-id="0eae7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0eae7-114">PARAMETERS</span></span>

### <span data-ttu-id="0eae7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eae7-115">-DefaultProfile</span></span>
<span data-ttu-id="0eae7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0eae7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eae7-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0eae7-117">-InputObject</span></span>
<span data-ttu-id="0eae7-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0eae7-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: LinkViaIdentity, LinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="0eae7-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="0eae7-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="0eae7-120">Maksymalna liczba nabyć przez abonentów</span><span class="sxs-lookup"><span data-stu-id="0eae7-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0eae7-121">-Offername</span><span class="sxs-lookup"><span data-stu-id="0eae7-121">-OfferName</span></span>
<span data-ttu-id="0eae7-122">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="0eae7-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0eae7-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="0eae7-123">-PlanLink</span></span>
<span data-ttu-id="0eae7-124">Definicja łączenia i odłączania planów do ofert.</span><span class="sxs-lookup"><span data-stu-id="0eae7-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="0eae7-125">Aby skonstruować, zobacz sekcję notatki dla właściwości PLANLINK i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="0eae7-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Link, LinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="0eae7-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="0eae7-126">-PlanLinkType</span></span>
<span data-ttu-id="0eae7-127">Typ linku planu.</span><span class="sxs-lookup"><span data-stu-id="0eae7-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0eae7-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="0eae7-128">-PlanName</span></span>
<span data-ttu-id="0eae7-129">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="0eae7-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0eae7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eae7-130">-ResourceGroupName</span></span>
<span data-ttu-id="0eae7-131">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="0eae7-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0eae7-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0eae7-132">-SubscriptionId</span></span>
<span data-ttu-id="0eae7-133">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="0eae7-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0eae7-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0eae7-134">-Confirm</span></span>
<span data-ttu-id="0eae7-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eae7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eae7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eae7-136">-WhatIf</span></span>
<span data-ttu-id="0eae7-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eae7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eae7-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0eae7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eae7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eae7-139">CommonParameters</span></span>
<span data-ttu-id="0eae7-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eae7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eae7-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eae7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eae7-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0eae7-142">INPUTS</span></span>

### <span data-ttu-id="0eae7-143">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="0eae7-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="0eae7-144">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0eae7-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="0eae7-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0eae7-145">OUTPUTS</span></span>

### <span data-ttu-id="0eae7-146">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="0eae7-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="0eae7-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0eae7-147">ALIASES</span></span>

## <span data-ttu-id="0eae7-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0eae7-148">NOTES</span></span>

<span data-ttu-id="0eae7-149">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0eae7-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0eae7-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0eae7-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0eae7-151">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="0eae7-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0eae7-152">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="0eae7-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="0eae7-153">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="0eae7-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="0eae7-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0eae7-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0eae7-155">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="0eae7-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="0eae7-156">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="0eae7-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="0eae7-157">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="0eae7-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="0eae7-158">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="0eae7-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="0eae7-159">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="0eae7-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="0eae7-160">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="0eae7-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="0eae7-161">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="0eae7-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="0eae7-162">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="0eae7-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="0eae7-163">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="0eae7-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="0eae7-164">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="0eae7-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0eae7-165">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0eae7-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="0eae7-166">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="0eae7-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="0eae7-167">PLANLINK <IPlanLinkDefinition> : definicja łączenia i odłączania planów z ofertami.</span><span class="sxs-lookup"><span data-stu-id="0eae7-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="0eae7-168">`[MaxAcquisitionCount <Int32?>]`: Maksymalna liczba zakupów według subskrybentów</span><span class="sxs-lookup"><span data-stu-id="0eae7-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="0eae7-169">`[PlanLinkType <PlanLinkType?>]`: Typ linku planu.</span><span class="sxs-lookup"><span data-stu-id="0eae7-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="0eae7-170">`[PlanName <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="0eae7-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="0eae7-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0eae7-171">RELATED LINKS</span></span>

