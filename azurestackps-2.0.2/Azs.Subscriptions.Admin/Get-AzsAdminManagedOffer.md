---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsadminmanagedoffer
schema: 2.0.0
ms.openlocfilehash: 79cac7a530a9aedc1e53120b29eb2dd8cb73489b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061562"
---
# <span data-ttu-id="50f5b-101">Get-AzsAdminManagedOffer</span><span class="sxs-lookup"><span data-stu-id="50f5b-101">Get-AzsAdminManagedOffer</span></span>

## <span data-ttu-id="50f5b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="50f5b-103">Uzyskaj określoną ofertę.</span><span class="sxs-lookup"><span data-stu-id="50f5b-103">Get the specified offer.</span></span>

## <span data-ttu-id="50f5b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50f5b-104">SYNTAX</span></span>

### <span data-ttu-id="50f5b-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="50f5b-105">List (Default)</span></span>
```
Get-AzsAdminManagedOffer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="50f5b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="50f5b-106">Get</span></span>
```
Get-AzsAdminManagedOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="50f5b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="50f5b-107">GetViaIdentity</span></span>
```
Get-AzsAdminManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="50f5b-108">List1</span><span class="sxs-lookup"><span data-stu-id="50f5b-108">List1</span></span>
```
Get-AzsAdminManagedOffer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="50f5b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="50f5b-109">DESCRIPTION</span></span>
<span data-ttu-id="50f5b-110">Uzyskaj określoną ofertę.</span><span class="sxs-lookup"><span data-stu-id="50f5b-110">Get the specified offer.</span></span>

## <span data-ttu-id="50f5b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50f5b-111">EXAMPLES</span></span>

### <span data-ttu-id="50f5b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50f5b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsAdminManagedOffer -Name "testoffer" -ResourceGroupName "testrg"

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="50f5b-113">Uzyskaj ofertę według imienia i nazwiska i ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f5b-113">Get offer by Name and ResourceGroupName</span></span>

## <span data-ttu-id="50f5b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50f5b-114">PARAMETERS</span></span>

### <span data-ttu-id="50f5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f5b-115">-DefaultProfile</span></span>
<span data-ttu-id="50f5b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50f5b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50f5b-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="50f5b-117">-InputObject</span></span>
<span data-ttu-id="50f5b-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="50f5b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="50f5b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50f5b-119">-Name</span></span>
<span data-ttu-id="50f5b-120">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="50f5b-120">Name of an offer.</span></span>

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

### <span data-ttu-id="50f5b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f5b-121">-ResourceGroupName</span></span>
<span data-ttu-id="50f5b-122">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="50f5b-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="50f5b-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="50f5b-123">-SubscriptionId</span></span>
<span data-ttu-id="50f5b-124">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="50f5b-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="50f5b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f5b-125">CommonParameters</span></span>
<span data-ttu-id="50f5b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f5b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f5b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50f5b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f5b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50f5b-128">INPUTS</span></span>

### <span data-ttu-id="50f5b-129">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="50f5b-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="50f5b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50f5b-130">OUTPUTS</span></span>

### <span data-ttu-id="50f5b-131">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="50f5b-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="50f5b-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="50f5b-132">ALIASES</span></span>

<span data-ttu-id="50f5b-133">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="50f5b-133">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="50f5b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50f5b-134">NOTES</span></span>

<span data-ttu-id="50f5b-135">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="50f5b-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50f5b-136">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="50f5b-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="50f5b-137">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="50f5b-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="50f5b-138">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="50f5b-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="50f5b-139">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="50f5b-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="50f5b-140">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="50f5b-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="50f5b-141">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="50f5b-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="50f5b-142">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="50f5b-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="50f5b-143">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="50f5b-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="50f5b-144">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="50f5b-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="50f5b-145">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="50f5b-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="50f5b-146">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="50f5b-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="50f5b-147">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="50f5b-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="50f5b-148">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="50f5b-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="50f5b-149">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="50f5b-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="50f5b-150">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="50f5b-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="50f5b-151">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="50f5b-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="50f5b-152">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="50f5b-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="50f5b-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50f5b-153">RELATED LINKS</span></span>

