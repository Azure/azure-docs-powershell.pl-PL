---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: e9de73f68501071bceb87c115c2c9882fc5ea988
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054081"
---
# <span data-ttu-id="332f3-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="332f3-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="332f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="332f3-102">SYNOPSIS</span></span>
<span data-ttu-id="332f3-103">Usuwanie określonej delegacji oferty.</span><span class="sxs-lookup"><span data-stu-id="332f3-103">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="332f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="332f3-104">SYNTAX</span></span>

### <span data-ttu-id="332f3-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="332f3-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="332f3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="332f3-106">DeleteViaIdentity</span></span>
```
Remove-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="332f3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="332f3-107">DESCRIPTION</span></span>
<span data-ttu-id="332f3-108">Usuwanie określonej delegacji oferty.</span><span class="sxs-lookup"><span data-stu-id="332f3-108">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="332f3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="332f3-109">EXAMPLES</span></span>

### <span data-ttu-id="332f3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="332f3-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1

{{ Add output here }}
```

<span data-ttu-id="332f3-111">Usuwa delegowanie oferty</span><span class="sxs-lookup"><span data-stu-id="332f3-111">Removes the offer delegation</span></span>

## <span data-ttu-id="332f3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="332f3-112">PARAMETERS</span></span>

### <span data-ttu-id="332f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="332f3-113">-DefaultProfile</span></span>
<span data-ttu-id="332f3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="332f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="332f3-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="332f3-115">-InputObject</span></span>
<span data-ttu-id="332f3-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="332f3-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="332f3-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="332f3-117">-Name</span></span>
<span data-ttu-id="332f3-118">Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="332f3-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="332f3-119">-Offername</span><span class="sxs-lookup"><span data-stu-id="332f3-119">-OfferName</span></span>
<span data-ttu-id="332f3-120">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="332f3-120">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="332f3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="332f3-121">-PassThru</span></span>
<span data-ttu-id="332f3-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="332f3-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="332f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="332f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="332f3-124">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="332f3-124">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="332f3-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="332f3-125">-SubscriptionId</span></span>
<span data-ttu-id="332f3-126">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="332f3-126">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="332f3-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="332f3-127">-Confirm</span></span>
<span data-ttu-id="332f3-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="332f3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="332f3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="332f3-129">-WhatIf</span></span>
<span data-ttu-id="332f3-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="332f3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="332f3-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="332f3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="332f3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="332f3-132">CommonParameters</span></span>
<span data-ttu-id="332f3-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="332f3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="332f3-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="332f3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="332f3-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="332f3-135">INPUTS</span></span>

### <span data-ttu-id="332f3-136">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="332f3-136">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="332f3-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="332f3-137">OUTPUTS</span></span>

### <span data-ttu-id="332f3-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="332f3-138">System.Boolean</span></span>

<span data-ttu-id="332f3-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="332f3-139">ALIASES</span></span>

## <span data-ttu-id="332f3-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="332f3-140">NOTES</span></span>

<span data-ttu-id="332f3-141">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="332f3-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="332f3-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="332f3-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="332f3-143">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="332f3-143">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="332f3-144">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="332f3-144">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="332f3-145">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="332f3-145">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="332f3-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="332f3-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="332f3-147">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="332f3-147">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="332f3-148">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="332f3-148">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="332f3-149">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="332f3-149">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="332f3-150">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="332f3-150">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="332f3-151">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="332f3-151">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="332f3-152">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="332f3-152">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="332f3-153">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="332f3-153">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="332f3-154">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="332f3-154">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="332f3-155">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="332f3-155">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="332f3-156">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="332f3-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="332f3-157">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="332f3-157">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="332f3-158">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="332f3-158">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="332f3-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="332f3-159">RELATED LINKS</span></span>

