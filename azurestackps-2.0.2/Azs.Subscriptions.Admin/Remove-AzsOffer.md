---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsoffer
schema: 2.0.0
ms.openlocfilehash: d38c7493e49888fe638cae4fbb5cb937ec41ccba
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055570"
---
# <span data-ttu-id="719cf-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="719cf-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="719cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="719cf-102">SYNOPSIS</span></span>
<span data-ttu-id="719cf-103">Usuwanie określonej oferty.</span><span class="sxs-lookup"><span data-stu-id="719cf-103">Delete the specified offer.</span></span>

## <span data-ttu-id="719cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="719cf-104">SYNTAX</span></span>

### <span data-ttu-id="719cf-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="719cf-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="719cf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="719cf-106">DeleteViaIdentity</span></span>
```
Remove-AzsOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="719cf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="719cf-107">DESCRIPTION</span></span>
<span data-ttu-id="719cf-108">Usuwanie określonej oferty.</span><span class="sxs-lookup"><span data-stu-id="719cf-108">Delete the specified offer.</span></span>

## <span data-ttu-id="719cf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="719cf-109">EXAMPLES</span></span>

### <span data-ttu-id="719cf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="719cf-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOffer -Name "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="719cf-111">Usuwanie określonej oferty.</span><span class="sxs-lookup"><span data-stu-id="719cf-111">Delete the specified offer.</span></span>

## <span data-ttu-id="719cf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="719cf-112">PARAMETERS</span></span>

### <span data-ttu-id="719cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="719cf-113">-DefaultProfile</span></span>
<span data-ttu-id="719cf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="719cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="719cf-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="719cf-115">-InputObject</span></span>
<span data-ttu-id="719cf-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="719cf-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="719cf-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="719cf-117">-Name</span></span>
<span data-ttu-id="719cf-118">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="719cf-118">Name of an offer.</span></span>

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

### <span data-ttu-id="719cf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="719cf-119">-PassThru</span></span>
<span data-ttu-id="719cf-120">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="719cf-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="719cf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="719cf-121">-ResourceGroupName</span></span>
<span data-ttu-id="719cf-122">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="719cf-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="719cf-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="719cf-123">-SubscriptionId</span></span>
<span data-ttu-id="719cf-124">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="719cf-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="719cf-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="719cf-125">-Confirm</span></span>
<span data-ttu-id="719cf-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="719cf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="719cf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="719cf-127">-WhatIf</span></span>
<span data-ttu-id="719cf-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="719cf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="719cf-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="719cf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="719cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="719cf-130">CommonParameters</span></span>
<span data-ttu-id="719cf-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="719cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="719cf-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="719cf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="719cf-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="719cf-133">INPUTS</span></span>

### <span data-ttu-id="719cf-134">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="719cf-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="719cf-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="719cf-135">OUTPUTS</span></span>

### <span data-ttu-id="719cf-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="719cf-136">System.Boolean</span></span>

<span data-ttu-id="719cf-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="719cf-137">ALIASES</span></span>

## <span data-ttu-id="719cf-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="719cf-138">NOTES</span></span>

<span data-ttu-id="719cf-139">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="719cf-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="719cf-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="719cf-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="719cf-141">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="719cf-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="719cf-142">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="719cf-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="719cf-143">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="719cf-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="719cf-144">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="719cf-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="719cf-145">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="719cf-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="719cf-146">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="719cf-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="719cf-147">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="719cf-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="719cf-148">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="719cf-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="719cf-149">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="719cf-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="719cf-150">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="719cf-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="719cf-151">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="719cf-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="719cf-152">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="719cf-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="719cf-153">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="719cf-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="719cf-154">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="719cf-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="719cf-155">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="719cf-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="719cf-156">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="719cf-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="719cf-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="719cf-157">RELATED LINKS</span></span>

