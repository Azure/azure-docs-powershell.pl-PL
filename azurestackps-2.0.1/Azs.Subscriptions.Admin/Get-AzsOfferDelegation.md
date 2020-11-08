---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 995d7296ef1e5b6f846d5343fd072909a877b1ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054253"
---
# <span data-ttu-id="f4540-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="f4540-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="f4540-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4540-102">SYNOPSIS</span></span>
<span data-ttu-id="f4540-103">Uzyskaj określoną delegację oferty.</span><span class="sxs-lookup"><span data-stu-id="f4540-103">Get the specified offer delegation.</span></span>

## <span data-ttu-id="f4540-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4540-104">SYNTAX</span></span>

### <span data-ttu-id="f4540-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f4540-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4540-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f4540-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4540-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f4540-107">GetViaIdentity</span></span>
```
Get-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4540-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f4540-108">DESCRIPTION</span></span>
<span data-ttu-id="f4540-109">Uzyskaj określoną delegację oferty.</span><span class="sxs-lookup"><span data-stu-id="f4540-109">Get the specified offer delegation.</span></span>

## <span data-ttu-id="f4540-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4540-110">EXAMPLES</span></span>

### <span data-ttu-id="f4540-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f4540-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferDelegation -OfferName "delegatedoffer" -ResourceGroupName "testrg"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/delegatedoffer/offerDelegations/offerdelegation
Location       : redmond
Name           : delegatedoffer/offerdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cbb018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="f4540-112">Pobierz listę delegowanych ofert.</span><span class="sxs-lookup"><span data-stu-id="f4540-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="f4540-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4540-113">PARAMETERS</span></span>

### <span data-ttu-id="f4540-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4540-114">-DefaultProfile</span></span>
<span data-ttu-id="f4540-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4540-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4540-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4540-116">-InputObject</span></span>
<span data-ttu-id="f4540-117">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f4540-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f4540-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4540-118">-Name</span></span>
<span data-ttu-id="f4540-119">Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="f4540-119">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4540-120">-Offername</span><span class="sxs-lookup"><span data-stu-id="f4540-120">-OfferName</span></span>
<span data-ttu-id="f4540-121">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="f4540-121">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4540-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4540-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4540-123">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="f4540-123">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4540-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f4540-124">-SubscriptionId</span></span>
<span data-ttu-id="f4540-125">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f4540-125">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4540-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4540-126">CommonParameters</span></span>
<span data-ttu-id="f4540-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4540-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4540-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4540-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4540-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4540-129">INPUTS</span></span>

### <span data-ttu-id="f4540-130">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f4540-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="f4540-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4540-131">OUTPUTS</span></span>

### <span data-ttu-id="f4540-132">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="f4540-132">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="f4540-133">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f4540-133">ALIASES</span></span>

## <span data-ttu-id="f4540-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4540-134">NOTES</span></span>

<span data-ttu-id="f4540-135">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f4540-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4540-136">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4540-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f4540-137">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f4540-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4540-138">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="f4540-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="f4540-139">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f4540-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="f4540-140">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f4540-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4540-141">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="f4540-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="f4540-142">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="f4540-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="f4540-143">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="f4540-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="f4540-144">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="f4540-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="f4540-145">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="f4540-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="f4540-146">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="f4540-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="f4540-147">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="f4540-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="f4540-148">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="f4540-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="f4540-149">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="f4540-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="f4540-150">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f4540-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f4540-151">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f4540-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="f4540-152">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="f4540-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="f4540-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4540-153">RELATED LINKS</span></span>

