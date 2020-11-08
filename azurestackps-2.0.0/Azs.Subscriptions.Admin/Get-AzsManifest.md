---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsmanifest
schema: 2.0.0
ms.openlocfilehash: 4e5ccedc67af31c19d35e5a91fad62ba46535ed7
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054096"
---
# <span data-ttu-id="2428a-101">Get-AzsManifest</span><span class="sxs-lookup"><span data-stu-id="2428a-101">Get-AzsManifest</span></span>

## <span data-ttu-id="2428a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2428a-102">SYNOPSIS</span></span>
<span data-ttu-id="2428a-103">Pobieranie określonego manifestu.</span><span class="sxs-lookup"><span data-stu-id="2428a-103">Get the specified manifest.</span></span>

## <span data-ttu-id="2428a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2428a-104">SYNTAX</span></span>

### <span data-ttu-id="2428a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2428a-105">List (Default)</span></span>
```
Get-AzsManifest [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2428a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2428a-106">Get</span></span>
```
Get-AzsManifest -ManifestName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2428a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2428a-107">GetViaIdentity</span></span>
```
Get-AzsManifest -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2428a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2428a-108">DESCRIPTION</span></span>
<span data-ttu-id="2428a-109">Pobieranie określonego manifestu.</span><span class="sxs-lookup"><span data-stu-id="2428a-109">Get the specified manifest.</span></span>

## <span data-ttu-id="2428a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2428a-110">EXAMPLES</span></span>

### <span data-ttu-id="2428a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2428a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsManifest

Name     : Microsoft-Authorization-Admin--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata

Name     : Microsoft-Authorization--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata
```

<span data-ttu-id="2428a-112">Wyświetla listę wszystkich manifestów w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="2428a-112">Lists all the manifests under the current subscription.</span></span>

## <span data-ttu-id="2428a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2428a-113">PARAMETERS</span></span>

### <span data-ttu-id="2428a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2428a-114">-DefaultProfile</span></span>
<span data-ttu-id="2428a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2428a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2428a-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2428a-116">-InputObject</span></span>
<span data-ttu-id="2428a-117">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2428a-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2428a-118">-Manifestname</span><span class="sxs-lookup"><span data-stu-id="2428a-118">-ManifestName</span></span>
<span data-ttu-id="2428a-119">Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="2428a-119">The manifest name.</span></span>

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

### <span data-ttu-id="2428a-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2428a-120">-SubscriptionId</span></span>
<span data-ttu-id="2428a-121">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2428a-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2428a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2428a-122">CommonParameters</span></span>
<span data-ttu-id="2428a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2428a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2428a-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2428a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2428a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2428a-125">INPUTS</span></span>

### <span data-ttu-id="2428a-126">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2428a-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="2428a-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2428a-127">OUTPUTS</span></span>

### <span data-ttu-id="2428a-128">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IManifest</span><span class="sxs-lookup"><span data-stu-id="2428a-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IManifest</span></span>

<span data-ttu-id="2428a-129">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2428a-129">ALIASES</span></span>

## <span data-ttu-id="2428a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2428a-130">NOTES</span></span>

<span data-ttu-id="2428a-131">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2428a-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2428a-132">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2428a-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2428a-133">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2428a-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2428a-134">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="2428a-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="2428a-135">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="2428a-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="2428a-136">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2428a-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2428a-137">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="2428a-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="2428a-138">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="2428a-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="2428a-139">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="2428a-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="2428a-140">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="2428a-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="2428a-141">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="2428a-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="2428a-142">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="2428a-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="2428a-143">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="2428a-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="2428a-144">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="2428a-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="2428a-145">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="2428a-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="2428a-146">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2428a-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2428a-147">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2428a-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="2428a-148">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="2428a-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="2428a-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2428a-149">RELATED LINKS</span></span>

