---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azssubscriptionquota
schema: 2.0.0
ms.openlocfilehash: 8e1c03393c1d276f5c93425250bf7202e49022d8
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054053"
---
# <span data-ttu-id="2cbaf-101">Get-AzsSubscriptionQuota</span><span class="sxs-lookup"><span data-stu-id="2cbaf-101">Get-AzsSubscriptionQuota</span></span>

## <span data-ttu-id="2cbaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbaf-103">Pobiera przydział według nazwy.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-103">Gets a quota by name.</span></span>

## <span data-ttu-id="2cbaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cbaf-104">SYNTAX</span></span>

### <span data-ttu-id="2cbaf-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2cbaf-105">List (Default)</span></span>
```
Get-AzsSubscriptionQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cbaf-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2cbaf-106">Get</span></span>
```
Get-AzsSubscriptionQuota -Quota <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2cbaf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2cbaf-107">GetViaIdentity</span></span>
```
Get-AzsSubscriptionQuota -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cbaf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2cbaf-108">DESCRIPTION</span></span>
<span data-ttu-id="2cbaf-109">Pobiera przydział według nazwy.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-109">Gets a quota by name.</span></span>

## <span data-ttu-id="2cbaf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cbaf-110">EXAMPLES</span></span>

### <span data-ttu-id="2cbaf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2cbaf-111">Example 1</span></span>
```powershell

```

<span data-ttu-id="2cbaf-112">Pobierz listę przydziałów dostawców zasobów abonamentu.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-112">Get the list of subscription resource provider quotas.</span></span>

## <span data-ttu-id="2cbaf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cbaf-113">PARAMETERS</span></span>

### <span data-ttu-id="2cbaf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cbaf-114">-DefaultProfile</span></span>
<span data-ttu-id="2cbaf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cbaf-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2cbaf-116">-InputObject</span></span>
<span data-ttu-id="2cbaf-117">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2cbaf-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2cbaf-118">-Location</span></span>
<span data-ttu-id="2cbaf-119">Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2cbaf-120">-Przydział</span><span class="sxs-lookup"><span data-stu-id="2cbaf-120">-Quota</span></span>
<span data-ttu-id="2cbaf-121">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-121">Name of the quota.</span></span>

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

### <span data-ttu-id="2cbaf-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2cbaf-122">-SubscriptionId</span></span>
<span data-ttu-id="2cbaf-123">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2cbaf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbaf-124">CommonParameters</span></span>
<span data-ttu-id="2cbaf-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbaf-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cbaf-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbaf-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cbaf-127">INPUTS</span></span>

### <span data-ttu-id="2cbaf-128">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2cbaf-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="2cbaf-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cbaf-129">OUTPUTS</span></span>

### <span data-ttu-id="2cbaf-130">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IQuota</span><span class="sxs-lookup"><span data-stu-id="2cbaf-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IQuota</span></span>

<span data-ttu-id="2cbaf-131">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2cbaf-131">ALIASES</span></span>

<span data-ttu-id="2cbaf-132">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="2cbaf-132">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="2cbaf-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cbaf-133">NOTES</span></span>

<span data-ttu-id="2cbaf-134">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2cbaf-135">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2cbaf-136">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2cbaf-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2cbaf-137">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="2cbaf-138">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="2cbaf-139">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2cbaf-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2cbaf-140">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="2cbaf-141">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="2cbaf-142">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="2cbaf-143">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="2cbaf-144">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="2cbaf-145">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="2cbaf-146">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="2cbaf-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="2cbaf-147">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="2cbaf-148">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="2cbaf-149">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2cbaf-150">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="2cbaf-151">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="2cbaf-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cbaf-152">RELATED LINKS</span></span>

