---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovidermanagedoffer
schema: 2.0.0
ms.openlocfilehash: 238fe2a9c3f0cf1d4fdefc5a09231066152cfe60
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054203"
---
# <span data-ttu-id="05791-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="05791-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="05791-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05791-102">SYNOPSIS</span></span>
<span data-ttu-id="05791-103">Pobierz określoną ofertę delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="05791-103">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="05791-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05791-104">SYNTAX</span></span>

### <span data-ttu-id="05791-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="05791-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="05791-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="05791-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> -Name <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="05791-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="05791-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="05791-108">Opis</span><span class="sxs-lookup"><span data-stu-id="05791-108">DESCRIPTION</span></span>
<span data-ttu-id="05791-109">Pobierz określoną ofertę delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="05791-109">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="05791-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05791-110">EXAMPLES</span></span>

### <span data-ttu-id="05791-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05791-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

{{ Add output here }}
```

<span data-ttu-id="05791-112">Pobierz listę ofert delegowanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="05791-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="05791-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05791-113">PARAMETERS</span></span>

### <span data-ttu-id="05791-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05791-114">-DefaultProfile</span></span>
<span data-ttu-id="05791-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05791-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05791-116">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05791-116">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="05791-117">Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="05791-117">Delegated provider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: DelegatedProviderId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05791-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="05791-118">-InputObject</span></span>
<span data-ttu-id="05791-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="05791-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05791-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05791-120">-Name</span></span>
<span data-ttu-id="05791-121">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="05791-121">Name of an offer.</span></span>

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

### <span data-ttu-id="05791-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="05791-122">-SubscriptionId</span></span>
<span data-ttu-id="05791-123">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="05791-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="05791-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05791-124">CommonParameters</span></span>
<span data-ttu-id="05791-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05791-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05791-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05791-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05791-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05791-127">INPUTS</span></span>

### <span data-ttu-id="05791-128">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="05791-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="05791-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05791-129">OUTPUTS</span></span>

### <span data-ttu-id="05791-130">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="05791-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDelegatedProviderOffer</span></span>

<span data-ttu-id="05791-131">PISUJE</span><span class="sxs-lookup"><span data-stu-id="05791-131">ALIASES</span></span>

## <span data-ttu-id="05791-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05791-132">NOTES</span></span>

<span data-ttu-id="05791-133">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="05791-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05791-134">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="05791-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="05791-135">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="05791-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05791-136">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="05791-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="05791-137">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="05791-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="05791-138">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="05791-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05791-139">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="05791-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="05791-140">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="05791-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="05791-141">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="05791-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="05791-142">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="05791-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="05791-143">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="05791-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="05791-144">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="05791-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="05791-145">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="05791-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="05791-146">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="05791-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="05791-147">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="05791-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="05791-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="05791-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="05791-149">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="05791-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="05791-150">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="05791-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="05791-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05791-151">RELATED LINKS</span></span>

