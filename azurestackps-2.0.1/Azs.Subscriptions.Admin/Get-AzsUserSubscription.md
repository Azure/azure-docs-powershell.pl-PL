---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: a36406499be15c53e9bfabd8aa9abf56b2afa1c7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054305"
---
# <span data-ttu-id="ebec4-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="ebec4-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="ebec4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebec4-102">SYNOPSIS</span></span>
<span data-ttu-id="ebec4-103">Uzyskaj określoną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="ebec4-103">Get a specified subscription.</span></span>

## <span data-ttu-id="ebec4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebec4-104">SYNTAX</span></span>

### <span data-ttu-id="ebec4-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ebec4-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebec4-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ebec4-106">Get</span></span>
```
Get-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ebec4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ebec4-107">GetViaIdentity</span></span>
```
Get-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebec4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ebec4-108">DESCRIPTION</span></span>
<span data-ttu-id="ebec4-109">Uzyskaj określoną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="ebec4-109">Get a specified subscription.</span></span>

## <span data-ttu-id="ebec4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebec4-110">EXAMPLES</span></span>

### <span data-ttu-id="ebec4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ebec4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsUserSubscription | Select-Object -First 1 | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : DRPTestffbffbe5-test-test-test-test-test-test
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="ebec4-112">Pobieranie listy abonamentów użytkowników jako operatora.</span><span class="sxs-lookup"><span data-stu-id="ebec4-112">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="ebec4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebec4-113">PARAMETERS</span></span>

### <span data-ttu-id="ebec4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebec4-114">-DefaultProfile</span></span>
<span data-ttu-id="ebec4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebec4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebec4-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="ebec4-116">-Filter</span></span>
<span data-ttu-id="ebec4-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="ebec4-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ebec4-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ebec4-118">-InputObject</span></span>
<span data-ttu-id="ebec4-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ebec4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ebec4-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ebec4-120">-SubscriptionId</span></span>
<span data-ttu-id="ebec4-121">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ebec4-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ebec4-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ebec4-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="ebec4-123">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ebec4-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="ebec4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebec4-124">CommonParameters</span></span>
<span data-ttu-id="ebec4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebec4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebec4-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebec4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebec4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebec4-127">INPUTS</span></span>

### <span data-ttu-id="ebec4-128">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ebec4-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="ebec4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebec4-129">OUTPUTS</span></span>

### <span data-ttu-id="ebec4-130">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="ebec4-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="ebec4-131">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ebec4-131">ALIASES</span></span>

## <span data-ttu-id="ebec4-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebec4-132">NOTES</span></span>

<span data-ttu-id="ebec4-133">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ebec4-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ebec4-134">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ebec4-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ebec4-135">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ebec4-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ebec4-136">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="ebec4-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="ebec4-137">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="ebec4-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="ebec4-138">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ebec4-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ebec4-139">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="ebec4-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="ebec4-140">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="ebec4-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="ebec4-141">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="ebec4-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="ebec4-142">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="ebec4-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="ebec4-143">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="ebec4-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="ebec4-144">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="ebec4-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="ebec4-145">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="ebec4-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="ebec4-146">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="ebec4-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="ebec4-147">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="ebec4-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="ebec4-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ebec4-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ebec4-149">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ebec4-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="ebec4-150">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="ebec4-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="ebec4-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebec4-151">RELATED LINKS</span></span>

