---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 03fbbc38582bf301052074e674fa86abe97d6b61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055889"
---
# <span data-ttu-id="35948-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="35948-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="35948-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35948-102">SYNOPSIS</span></span>


## <span data-ttu-id="35948-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35948-103">SYNTAX</span></span>

### <span data-ttu-id="35948-104">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="35948-104">Delete (Default)</span></span>
```
Remove-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35948-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35948-105">DeleteViaIdentity</span></span>
```
Remove-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Force]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35948-106">Opis</span><span class="sxs-lookup"><span data-stu-id="35948-106">DESCRIPTION</span></span>


## <span data-ttu-id="35948-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35948-107">EXAMPLES</span></span>

### <span data-ttu-id="35948-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35948-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

```

<span data-ttu-id="35948-109">Usuwanie określonego abonamentu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="35948-109">Delete the specified tenant subscription.</span></span>

## <span data-ttu-id="35948-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35948-110">PARAMETERS</span></span>

### <span data-ttu-id="35948-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35948-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="35948-112">-Force</span><span class="sxs-lookup"><span data-stu-id="35948-112">-Force</span></span>


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

### <span data-ttu-id="35948-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35948-113">-InputObject</span></span>
<span data-ttu-id="35948-114">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="35948-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35948-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35948-115">-PassThru</span></span>


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

### <span data-ttu-id="35948-116">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="35948-116">-SubscriptionId</span></span>


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

### <span data-ttu-id="35948-117">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35948-117">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="35948-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35948-118">-Confirm</span></span>
<span data-ttu-id="35948-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35948-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35948-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35948-120">-WhatIf</span></span>
<span data-ttu-id="35948-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35948-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35948-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35948-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35948-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35948-123">CommonParameters</span></span>
<span data-ttu-id="35948-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35948-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35948-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35948-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35948-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35948-126">INPUTS</span></span>

### <span data-ttu-id="35948-127">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="35948-127">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="35948-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35948-128">OUTPUTS</span></span>

### <span data-ttu-id="35948-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35948-129">System.Boolean</span></span>

<span data-ttu-id="35948-130">PISUJE</span><span class="sxs-lookup"><span data-stu-id="35948-130">ALIASES</span></span>

## <span data-ttu-id="35948-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35948-131">NOTES</span></span>

<span data-ttu-id="35948-132">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="35948-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35948-133">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35948-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="35948-134">INPUTobject <ISubscriptionsAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="35948-134">INPUTOBJECT <ISubscriptionsAdminIdentity>:</span></span> 
  - <span data-ttu-id="35948-135">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="35948-135">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="35948-136">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="35948-136">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="35948-137">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="35948-137">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35948-138">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="35948-138">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="35948-139">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="35948-139">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="35948-140">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="35948-140">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="35948-141">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="35948-141">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="35948-142">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="35948-142">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="35948-143">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="35948-143">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="35948-144">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="35948-144">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="35948-145">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="35948-145">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="35948-146">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="35948-146">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="35948-147">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="35948-147">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="35948-148">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="35948-148">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="35948-149">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="35948-149">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="35948-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35948-150">RELATED LINKS</span></span>

