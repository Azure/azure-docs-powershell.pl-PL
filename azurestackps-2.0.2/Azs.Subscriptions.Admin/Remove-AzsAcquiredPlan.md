---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 80a4353497d0c7894a8c0ac4d95e57e56a6211a1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061550"
---
# <span data-ttu-id="8ff47-101">Remove-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="8ff47-101">Remove-AzsAcquiredPlan</span></span>

## <span data-ttu-id="8ff47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ff47-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff47-103">Usuwa nabyty plan.</span><span class="sxs-lookup"><span data-stu-id="8ff47-103">Deletes an acquired plan.</span></span>

## <span data-ttu-id="8ff47-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ff47-104">SYNTAX</span></span>

### <span data-ttu-id="8ff47-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8ff47-105">Delete (Default)</span></span>
```
Remove-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8ff47-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8ff47-106">DeleteViaIdentity</span></span>
```
Remove-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8ff47-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8ff47-107">DESCRIPTION</span></span>
<span data-ttu-id="8ff47-108">Usuwa nabyty plan.</span><span class="sxs-lookup"><span data-stu-id="8ff47-108">Deletes an acquired plan.</span></span>

## <span data-ttu-id="8ff47-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ff47-109">EXAMPLES</span></span>

### <span data-ttu-id="8ff47-110">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="8ff47-110">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsAcquiredPlan -PlanAcquisitionId "718c7f7c-4868-479a-98ce-5caaa8f158c2" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

```

<span data-ttu-id="8ff47-111">Usuwanie nabytego planu.</span><span class="sxs-lookup"><span data-stu-id="8ff47-111">Delete an acquired plan.</span></span>

## <span data-ttu-id="8ff47-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ff47-112">PARAMETERS</span></span>

### <span data-ttu-id="8ff47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff47-113">-DefaultProfile</span></span>
<span data-ttu-id="8ff47-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ff47-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ff47-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ff47-115">-InputObject</span></span>
<span data-ttu-id="8ff47-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8ff47-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8ff47-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ff47-117">-PassThru</span></span>
<span data-ttu-id="8ff47-118">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="8ff47-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8ff47-119">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="8ff47-119">-PlanAcquisitionId</span></span>
<span data-ttu-id="8ff47-120">Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="8ff47-120">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="8ff47-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8ff47-121">-SubscriptionId</span></span>
<span data-ttu-id="8ff47-122">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8ff47-122">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8ff47-123">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ff47-123">-TargetSubscriptionId</span></span>
<span data-ttu-id="8ff47-124">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8ff47-124">The target subscription ID.</span></span>

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

### <span data-ttu-id="8ff47-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ff47-125">-Confirm</span></span>
<span data-ttu-id="8ff47-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ff47-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ff47-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ff47-127">-WhatIf</span></span>
<span data-ttu-id="8ff47-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ff47-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ff47-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ff47-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ff47-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff47-130">CommonParameters</span></span>
<span data-ttu-id="8ff47-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ff47-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff47-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ff47-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff47-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ff47-133">INPUTS</span></span>

### <span data-ttu-id="8ff47-134">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8ff47-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="8ff47-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ff47-135">OUTPUTS</span></span>

### <span data-ttu-id="8ff47-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ff47-136">System.Boolean</span></span>

<span data-ttu-id="8ff47-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8ff47-137">ALIASES</span></span>

### <span data-ttu-id="8ff47-138">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="8ff47-138">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="8ff47-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ff47-139">NOTES</span></span>

<span data-ttu-id="8ff47-140">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8ff47-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ff47-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8ff47-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8ff47-142">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="8ff47-142">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8ff47-143">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="8ff47-143">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="8ff47-144">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="8ff47-144">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="8ff47-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8ff47-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ff47-146">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="8ff47-146">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="8ff47-147">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="8ff47-147">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="8ff47-148">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="8ff47-148">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="8ff47-149">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="8ff47-149">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="8ff47-150">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="8ff47-150">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="8ff47-151">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="8ff47-151">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="8ff47-152">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="8ff47-152">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="8ff47-153">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="8ff47-153">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="8ff47-154">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="8ff47-154">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="8ff47-155">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8ff47-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8ff47-156">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8ff47-156">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="8ff47-157">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="8ff47-157">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="8ff47-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ff47-158">RELATED LINKS</span></span>

