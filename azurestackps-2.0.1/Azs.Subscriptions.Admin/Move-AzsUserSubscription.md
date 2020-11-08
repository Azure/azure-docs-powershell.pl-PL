---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/move-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 51ad63ef1531e7494b3929b8508e88e988155081
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054304"
---
# <span data-ttu-id="80932-101">Move-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="80932-101">Move-AzsUserSubscription</span></span>

## <span data-ttu-id="80932-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80932-102">SYNOPSIS</span></span>
<span data-ttu-id="80932-103">Przenoszenie subskrypcji między delegowanymi ofertami dostawców.</span><span class="sxs-lookup"><span data-stu-id="80932-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="80932-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80932-104">SYNTAX</span></span>

### <span data-ttu-id="80932-105">MoveExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="80932-105">MoveExpanded (Default)</span></span>
```
Move-AzsUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80932-106">Przeniesione</span><span class="sxs-lookup"><span data-stu-id="80932-106">Move</span></span>
```
Move-AzsUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="80932-107">MoveViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80932-107">MoveViaIdentity</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80932-108">MoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="80932-108">MoveViaIdentityExpanded</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80932-109">Opis</span><span class="sxs-lookup"><span data-stu-id="80932-109">DESCRIPTION</span></span>
<span data-ttu-id="80932-110">Przenoszenie subskrypcji między delegowanymi ofertami dostawców.</span><span class="sxs-lookup"><span data-stu-id="80932-110">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="80932-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80932-111">EXAMPLES</span></span>

### <span data-ttu-id="80932-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80932-112">Example 1</span></span>
```powershell
PS C:\> Move-AzsSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

{{ Add output here }}
```

<span data-ttu-id="80932-113">Przenieś subskrypcje użytkowników do oferty delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="80932-113">Move user subscriptions to a delegated provider offer.</span></span>

### <span data-ttu-id="80932-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="80932-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id
Move-AzsSubscription -ResourceId $resourceIds

{{ Add output here }}
```

<span data-ttu-id="80932-115">Przenieś subskrypcje użytkowników z delegowanego dostawcy na domyślnego dostawcę.</span><span class="sxs-lookup"><span data-stu-id="80932-115">Move user subscriptions from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="80932-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80932-116">PARAMETERS</span></span>

### <span data-ttu-id="80932-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80932-117">-AsJob</span></span>
<span data-ttu-id="80932-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="80932-118">Run the command as a job</span></span>

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

### <span data-ttu-id="80932-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80932-119">-DefaultProfile</span></span>
<span data-ttu-id="80932-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80932-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80932-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="80932-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="80932-122">Identyfikator oferty delegowanego dostawcy (z kontekstu administratora), do którego mają być przenoszone subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="80932-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80932-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="80932-123">-InputObject</span></span>
<span data-ttu-id="80932-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="80932-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: MoveViaIdentity, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="80932-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="80932-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="80932-126">Definicja akcji Przenieś subskrypcje w celu skonstruowania, zobacz sekcję notatki dla właściwości MOVESUBSCRIPTIONSDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="80932-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Move, MoveViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="80932-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="80932-127">-NoWait</span></span>
<span data-ttu-id="80932-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="80932-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="80932-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80932-129">-PassThru</span></span>
<span data-ttu-id="80932-130">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="80932-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="80932-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80932-131">-ResourceId</span></span>
<span data-ttu-id="80932-132">Kolekcja subskrypcji przenoszonych do docelowej oferty delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="80932-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80932-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="80932-133">-SubscriptionId</span></span>
<span data-ttu-id="80932-134">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="80932-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Move, MoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80932-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80932-135">-Confirm</span></span>
<span data-ttu-id="80932-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80932-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80932-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80932-137">-WhatIf</span></span>
<span data-ttu-id="80932-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80932-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80932-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80932-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80932-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80932-140">CommonParameters</span></span>
<span data-ttu-id="80932-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80932-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80932-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80932-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80932-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80932-143">INPUTS</span></span>

### <span data-ttu-id="80932-144">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="80932-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="80932-145">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="80932-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="80932-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80932-146">OUTPUTS</span></span>

### <span data-ttu-id="80932-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80932-147">System.Boolean</span></span>

<span data-ttu-id="80932-148">PISUJE</span><span class="sxs-lookup"><span data-stu-id="80932-148">ALIASES</span></span>

## <span data-ttu-id="80932-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80932-149">NOTES</span></span>

<span data-ttu-id="80932-150">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="80932-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80932-151">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80932-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="80932-152">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="80932-152">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80932-153">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="80932-153">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="80932-154">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="80932-154">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="80932-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="80932-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80932-156">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="80932-156">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="80932-157">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="80932-157">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="80932-158">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="80932-158">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="80932-159">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="80932-159">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="80932-160">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="80932-160">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="80932-161">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="80932-161">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="80932-162">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="80932-162">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="80932-163">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="80932-163">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="80932-164">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="80932-164">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="80932-165">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="80932-165">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="80932-166">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="80932-166">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="80932-167">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="80932-167">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="80932-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : definicja akcji Przenieś subskrypcje</span><span class="sxs-lookup"><span data-stu-id="80932-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="80932-169">`Resources <String[]>`: Kolekcja subskrypcji, które mają zostać przeniesione do docelowej oferty delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="80932-169">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="80932-170">`[TargetDelegatedProviderOffer <String>]`: Identyfikator oferty delegowanego dostawcy (z kontekstu administratora), do którego mają być przenoszone subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="80932-170">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="80932-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80932-171">RELATED LINKS</span></span>

