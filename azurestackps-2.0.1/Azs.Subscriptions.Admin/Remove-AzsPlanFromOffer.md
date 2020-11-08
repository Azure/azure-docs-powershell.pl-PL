---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplanfromoffer
schema: 2.0.0
ms.openlocfilehash: c3a68c028abc9033cef9d9fd7e8fbd39e4066d2d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054166"
---
# <span data-ttu-id="d1639-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="d1639-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="d1639-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1639-102">SYNOPSIS</span></span>
<span data-ttu-id="d1639-103">Odłączanie planu od oferty.</span><span class="sxs-lookup"><span data-stu-id="d1639-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="d1639-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1639-104">SYNTAX</span></span>

### <span data-ttu-id="d1639-105">UnlinkExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d1639-105">UnlinkExpanded (Default)</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1639-106">Odłącz</span><span class="sxs-lookup"><span data-stu-id="d1639-106">Unlink</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1639-107">UnlinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1639-107">UnlinkViaIdentity</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1639-108">UnlinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d1639-108">UnlinkViaIdentityExpanded</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d1639-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d1639-109">DESCRIPTION</span></span>
<span data-ttu-id="d1639-110">Odłączanie planu od oferty.</span><span class="sxs-lookup"><span data-stu-id="d1639-110">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="d1639-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1639-111">EXAMPLES</span></span>

### <span data-ttu-id="d1639-112">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="d1639-112">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsPlanFromOffer -PlanName "testplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="d1639-113">Odłączanie planu od oferty.</span><span class="sxs-lookup"><span data-stu-id="d1639-113">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="d1639-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1639-114">PARAMETERS</span></span>

### <span data-ttu-id="d1639-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1639-115">-DefaultProfile</span></span>
<span data-ttu-id="d1639-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1639-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1639-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1639-117">-InputObject</span></span>
<span data-ttu-id="d1639-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d1639-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: UnlinkViaIdentity, UnlinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d1639-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="d1639-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="d1639-120">Maksymalna liczba nabyć przez abonentów</span><span class="sxs-lookup"><span data-stu-id="d1639-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1639-121">-Offername</span><span class="sxs-lookup"><span data-stu-id="d1639-121">-OfferName</span></span>
<span data-ttu-id="d1639-122">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="d1639-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1639-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="d1639-123">-PlanLink</span></span>
<span data-ttu-id="d1639-124">Definicja łączenia i odłączania planów do ofert.</span><span class="sxs-lookup"><span data-stu-id="d1639-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="d1639-125">Aby skonstruować, zobacz sekcję notatki dla właściwości PLANLINK i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="d1639-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Unlink, UnlinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d1639-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="d1639-126">-PlanLinkType</span></span>
<span data-ttu-id="d1639-127">Typ linku planu.</span><span class="sxs-lookup"><span data-stu-id="d1639-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1639-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d1639-128">-PlanName</span></span>
<span data-ttu-id="d1639-129">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="d1639-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1639-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1639-130">-ResourceGroupName</span></span>
<span data-ttu-id="d1639-131">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="d1639-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1639-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d1639-132">-SubscriptionId</span></span>
<span data-ttu-id="d1639-133">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d1639-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1639-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1639-134">-Confirm</span></span>
<span data-ttu-id="d1639-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1639-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1639-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1639-136">-WhatIf</span></span>
<span data-ttu-id="d1639-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1639-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1639-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d1639-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1639-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1639-139">CommonParameters</span></span>
<span data-ttu-id="d1639-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1639-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1639-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1639-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1639-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1639-142">INPUTS</span></span>

### <span data-ttu-id="d1639-143">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="d1639-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="d1639-144">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d1639-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="d1639-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1639-145">OUTPUTS</span></span>

### <span data-ttu-id="d1639-146">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="d1639-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="d1639-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d1639-147">ALIASES</span></span>

## <span data-ttu-id="d1639-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1639-148">NOTES</span></span>

<span data-ttu-id="d1639-149">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d1639-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1639-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1639-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d1639-151">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d1639-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1639-152">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="d1639-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="d1639-153">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="d1639-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="d1639-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d1639-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1639-155">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="d1639-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="d1639-156">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="d1639-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="d1639-157">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="d1639-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="d1639-158">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="d1639-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="d1639-159">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="d1639-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="d1639-160">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="d1639-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="d1639-161">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="d1639-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="d1639-162">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="d1639-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d1639-163">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="d1639-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="d1639-164">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d1639-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d1639-165">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="d1639-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="d1639-166">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="d1639-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="d1639-167">PLANLINK <IPlanLinkDefinition> : definicja łączenia i odłączania planów z ofertami.</span><span class="sxs-lookup"><span data-stu-id="d1639-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="d1639-168">`[MaxAcquisitionCount <Int32?>]`: Maksymalna liczba zakupów według subskrybentów</span><span class="sxs-lookup"><span data-stu-id="d1639-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="d1639-169">`[PlanLinkType <PlanLinkType?>]`: Typ linku planu.</span><span class="sxs-lookup"><span data-stu-id="d1639-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="d1639-170">`[PlanName <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="d1639-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="d1639-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1639-171">RELATED LINKS</span></span>

