---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054110"
---
# <span data-ttu-id="38f6c-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="38f6c-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="38f6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="38f6c-103">Pobiera określony plan uzyskany przez abonament zużywający ofertę.</span><span class="sxs-lookup"><span data-stu-id="38f6c-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="38f6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38f6c-104">SYNTAX</span></span>

### <span data-ttu-id="38f6c-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="38f6c-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="38f6c-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="38f6c-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="38f6c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="38f6c-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="38f6c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="38f6c-108">DESCRIPTION</span></span>
<span data-ttu-id="38f6c-109">Pobiera określony plan uzyskany przez abonament zużywający ofertę.</span><span class="sxs-lookup"><span data-stu-id="38f6c-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="38f6c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38f6c-110">EXAMPLES</span></span>

### <span data-ttu-id="38f6c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38f6c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsAcquiredPlan -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="38f6c-112">Pobierz zbiór wszystkich nabytych planów, do których subskrypcja ma dostęp.</span><span class="sxs-lookup"><span data-stu-id="38f6c-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="38f6c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38f6c-113">PARAMETERS</span></span>

### <span data-ttu-id="38f6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f6c-114">-DefaultProfile</span></span>
<span data-ttu-id="38f6c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38f6c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38f6c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="38f6c-116">-InputObject</span></span>
<span data-ttu-id="38f6c-117">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="38f6c-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="38f6c-118">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="38f6c-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="38f6c-119">Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="38f6c-119">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="38f6c-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="38f6c-120">-SubscriptionId</span></span>
<span data-ttu-id="38f6c-121">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="38f6c-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="38f6c-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38f6c-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="38f6c-123">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="38f6c-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="38f6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f6c-124">CommonParameters</span></span>
<span data-ttu-id="38f6c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f6c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38f6c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f6c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38f6c-127">INPUTS</span></span>

### <span data-ttu-id="38f6c-128">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="38f6c-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="38f6c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38f6c-129">OUTPUTS</span></span>

### <span data-ttu-id="38f6c-130">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="38f6c-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="38f6c-131">PISUJE</span><span class="sxs-lookup"><span data-stu-id="38f6c-131">ALIASES</span></span>

<span data-ttu-id="38f6c-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="38f6c-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="38f6c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38f6c-133">NOTES</span></span>

<span data-ttu-id="38f6c-134">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="38f6c-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38f6c-135">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38f6c-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="38f6c-136">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="38f6c-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38f6c-137">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="38f6c-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="38f6c-138">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="38f6c-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="38f6c-139">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="38f6c-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38f6c-140">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="38f6c-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="38f6c-141">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="38f6c-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="38f6c-142">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="38f6c-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="38f6c-143">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="38f6c-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="38f6c-144">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="38f6c-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="38f6c-145">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="38f6c-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="38f6c-146">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="38f6c-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="38f6c-147">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="38f6c-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="38f6c-148">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="38f6c-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="38f6c-149">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="38f6c-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="38f6c-150">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="38f6c-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="38f6c-151">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="38f6c-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="38f6c-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38f6c-152">RELATED LINKS</span></span>

