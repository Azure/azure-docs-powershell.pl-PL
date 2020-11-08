---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsmoveusersubscription
schema: 2.0.0
ms.openlocfilehash: c0e80b7d0f17bf505c0b3bb8d22539afffea851a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055970"
---
# <span data-ttu-id="c027a-101">Test-AzsMoveUserSubscription</span><span class="sxs-lookup"><span data-stu-id="c027a-101">Test-AzsMoveUserSubscription</span></span>

## <span data-ttu-id="c027a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c027a-102">SYNOPSIS</span></span>
<span data-ttu-id="c027a-103">Sprawdzanie, czy subskrypcje użytkowników mogą być przenoszone między ofertami delegowanych dostawców.</span><span class="sxs-lookup"><span data-stu-id="c027a-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="c027a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c027a-104">SYNTAX</span></span>

### <span data-ttu-id="c027a-105">ValidateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c027a-105">ValidateExpanded (Default)</span></span>
```
Test-AzsMoveUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c027a-106">Weryfikuje</span><span class="sxs-lookup"><span data-stu-id="c027a-106">Validate</span></span>
```
Test-AzsMoveUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c027a-107">ValidateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c027a-107">ValidateViaIdentity</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c027a-108">ValidateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c027a-108">ValidateViaIdentityExpanded</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c027a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c027a-109">DESCRIPTION</span></span>
<span data-ttu-id="c027a-110">Sprawdzanie, czy subskrypcje użytkowników mogą być przenoszone między ofertami delegowanych dostawców.</span><span class="sxs-lookup"><span data-stu-id="c027a-110">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="c027a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c027a-111">EXAMPLES</span></span>

### <span data-ttu-id="c027a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c027a-112">Example 1</span></span>
```powershell
PS C:\> Test-MoveUserSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

```

<span data-ttu-id="c027a-113">Przetestuj, czy subskrypcje użytkowników mogą być przenoszone do oferty delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c027a-113">Test that user subscriptions can be moved to a delegated provider offer.</span></span>

### <span data-ttu-id="c027a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c027a-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where Displayname -eq "testsubscription" | Select -ExpandProperty Id
Test-MoveUserSubscription -ResourceId $resourceIds

```

<span data-ttu-id="c027a-115">Przetestuj, czy subskrypcje użytkowników mogą być przenoszone przez dostawcę delegowanego na domyślnego dostawcę.</span><span class="sxs-lookup"><span data-stu-id="c027a-115">Test that user subscriptions can be moved from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="c027a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c027a-116">PARAMETERS</span></span>

### <span data-ttu-id="c027a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c027a-117">-AsJob</span></span>
<span data-ttu-id="c027a-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="c027a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c027a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c027a-119">-DefaultProfile</span></span>
<span data-ttu-id="c027a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c027a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c027a-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="c027a-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="c027a-122">Identyfikator oferty delegowanego dostawcy (z kontekstu administratora), do którego mają być przenoszone subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="c027a-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c027a-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c027a-123">-InputObject</span></span>
<span data-ttu-id="c027a-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c027a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: ValidateViaIdentity, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c027a-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="c027a-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="c027a-126">Definicja akcji Przenieś subskrypcje w celu skonstruowania, zobacz sekcję notatki dla właściwości MOVESUBSCRIPTIONSDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="c027a-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Validate, ValidateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c027a-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c027a-127">-NoWait</span></span>
<span data-ttu-id="c027a-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="c027a-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c027a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c027a-129">-PassThru</span></span>
<span data-ttu-id="c027a-130">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="c027a-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c027a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c027a-131">-ResourceId</span></span>
<span data-ttu-id="c027a-132">Kolekcja subskrypcji przenoszonych do docelowej oferty delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c027a-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c027a-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c027a-133">-SubscriptionId</span></span>
<span data-ttu-id="c027a-134">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c027a-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Validate, ValidateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c027a-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c027a-135">-Confirm</span></span>
<span data-ttu-id="c027a-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c027a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c027a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c027a-137">-WhatIf</span></span>
<span data-ttu-id="c027a-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c027a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c027a-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c027a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c027a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c027a-140">CommonParameters</span></span>
<span data-ttu-id="c027a-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c027a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c027a-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c027a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c027a-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c027a-143">INPUTS</span></span>

### <span data-ttu-id="c027a-144">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="c027a-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="c027a-145">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c027a-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="c027a-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c027a-146">OUTPUTS</span></span>

### <span data-ttu-id="c027a-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c027a-147">System.Boolean</span></span>

<span data-ttu-id="c027a-148">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c027a-148">ALIASES</span></span>

### <span data-ttu-id="c027a-149">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="c027a-149">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="c027a-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c027a-150">NOTES</span></span>

<span data-ttu-id="c027a-151">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c027a-151">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c027a-152">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c027a-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c027a-153">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="c027a-153">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c027a-154">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="c027a-154">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="c027a-155">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c027a-155">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="c027a-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c027a-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c027a-157">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="c027a-157">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="c027a-158">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="c027a-158">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="c027a-159">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="c027a-159">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="c027a-160">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="c027a-160">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="c027a-161">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="c027a-161">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="c027a-162">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="c027a-162">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="c027a-163">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="c027a-163">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="c027a-164">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="c027a-164">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c027a-165">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="c027a-165">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="c027a-166">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c027a-166">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c027a-167">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c027a-167">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="c027a-168">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="c027a-168">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="c027a-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : definicja akcji Przenieś subskrypcje</span><span class="sxs-lookup"><span data-stu-id="c027a-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="c027a-170">`Resources <String[]>`: Kolekcja subskrypcji, które mają zostać przeniesione do docelowej oferty delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c027a-170">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="c027a-171">`[TargetDelegatedProviderOffer <String>]`: Identyfikator oferty delegowanego dostawcy (z kontekstu administratora), do którego mają być przenoszone subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="c027a-171">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="c027a-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c027a-172">RELATED LINKS</span></span>

