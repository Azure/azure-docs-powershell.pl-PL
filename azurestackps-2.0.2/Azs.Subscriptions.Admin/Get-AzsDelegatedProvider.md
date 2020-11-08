---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovider
schema: 2.0.0
ms.openlocfilehash: 2c6c87ce0b40fae228756d4a9dd452b49ce1aad2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061591"
---
# <span data-ttu-id="b30a1-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="b30a1-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="b30a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b30a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b30a1-103">Uzyskaj określonego dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="b30a1-103">Get the specified delegated provider.</span></span>

## <span data-ttu-id="b30a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b30a1-104">SYNTAX</span></span>

### <span data-ttu-id="b30a1-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b30a1-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b30a1-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b30a1-106">Get</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b30a1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b30a1-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProvider -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b30a1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b30a1-108">DESCRIPTION</span></span>
<span data-ttu-id="b30a1-109">Uzyskaj określonego dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="b30a1-109">Get the specified delegated provider.</span></span>

## <span data-ttu-id="b30a1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b30a1-110">EXAMPLES</span></span>

### <span data-ttu-id="b30a1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b30a1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProvider -DelegatedProviderId "ed3e275b-87d1-4e94-9962-b3700287bdbc" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : cnur4866tenantresellersubscription843
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/cnur4866resellersubscrrg843/providers/Microsoft.Subscriptions.Admin/offers/cnur4866tenantsubsvcoffe
                                  r843
Owner                           : tenantadmin1@msazurestack.onmicrosoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="b30a1-112">Uzyskaj określonego dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="b30a1-112">Get a specific delegated provider.</span></span>

## <span data-ttu-id="b30a1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b30a1-113">PARAMETERS</span></span>

### <span data-ttu-id="b30a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30a1-114">-DefaultProfile</span></span>
<span data-ttu-id="b30a1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b30a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b30a1-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="b30a1-116">-DelegatedProviderId</span></span>
<span data-ttu-id="b30a1-117">Identyfikator DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="b30a1-117">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="b30a1-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b30a1-118">-InputObject</span></span>
<span data-ttu-id="b30a1-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b30a1-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b30a1-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b30a1-120">-SubscriptionId</span></span>
<span data-ttu-id="b30a1-121">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b30a1-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b30a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30a1-122">CommonParameters</span></span>
<span data-ttu-id="b30a1-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30a1-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b30a1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30a1-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b30a1-125">INPUTS</span></span>

### <span data-ttu-id="b30a1-126">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b30a1-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="b30a1-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b30a1-127">OUTPUTS</span></span>

### <span data-ttu-id="b30a1-128">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="b30a1-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="b30a1-129">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b30a1-129">ALIASES</span></span>

## <span data-ttu-id="b30a1-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b30a1-130">NOTES</span></span>

<span data-ttu-id="b30a1-131">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b30a1-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b30a1-132">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b30a1-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b30a1-133">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b30a1-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b30a1-134">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="b30a1-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="b30a1-135">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="b30a1-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="b30a1-136">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b30a1-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b30a1-137">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="b30a1-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="b30a1-138">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="b30a1-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="b30a1-139">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="b30a1-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="b30a1-140">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="b30a1-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="b30a1-141">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="b30a1-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="b30a1-142">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="b30a1-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="b30a1-143">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="b30a1-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="b30a1-144">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="b30a1-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b30a1-145">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="b30a1-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="b30a1-146">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b30a1-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b30a1-147">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b30a1-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="b30a1-148">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="b30a1-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="b30a1-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b30a1-149">RELATED LINKS</span></span>

