---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054122"
---
# <span data-ttu-id="3a622-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="3a622-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="3a622-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a622-102">SYNOPSIS</span></span>
<span data-ttu-id="3a622-103">Uzyskaj dzierżawę katalogu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3a622-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="3a622-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a622-104">SYNTAX</span></span>

### <span data-ttu-id="3a622-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3a622-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a622-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3a622-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a622-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a622-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a622-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3a622-108">DESCRIPTION</span></span>
<span data-ttu-id="3a622-109">Uzyskaj dzierżawę katalogu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3a622-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="3a622-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a622-110">EXAMPLES</span></span>

### <span data-ttu-id="3a622-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a622-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="3a622-112">Wyświetla listę wszystkich dzierżawców w katalogu w ramach bieżącego abonamentu i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a622-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="3a622-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a622-113">PARAMETERS</span></span>

### <span data-ttu-id="3a622-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a622-114">-DefaultProfile</span></span>
<span data-ttu-id="3a622-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a622-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a622-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a622-116">-InputObject</span></span>
<span data-ttu-id="3a622-117">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3a622-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a622-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a622-118">-Name</span></span>
<span data-ttu-id="3a622-119">Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="3a622-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="3a622-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a622-120">-ResourceGroupName</span></span>
<span data-ttu-id="3a622-121">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="3a622-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3a622-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3a622-122">-SubscriptionId</span></span>
<span data-ttu-id="3a622-123">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3a622-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3a622-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a622-124">CommonParameters</span></span>
<span data-ttu-id="3a622-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a622-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a622-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a622-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a622-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a622-127">INPUTS</span></span>

### <span data-ttu-id="3a622-128">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3a622-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="3a622-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a622-129">OUTPUTS</span></span>

### <span data-ttu-id="3a622-130">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="3a622-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="3a622-131">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3a622-131">ALIASES</span></span>

## <span data-ttu-id="3a622-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a622-132">NOTES</span></span>

<span data-ttu-id="3a622-133">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3a622-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a622-134">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a622-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3a622-135">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3a622-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a622-136">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="3a622-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="3a622-137">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="3a622-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="3a622-138">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3a622-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a622-139">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="3a622-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="3a622-140">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="3a622-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="3a622-141">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="3a622-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="3a622-142">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="3a622-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="3a622-143">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="3a622-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="3a622-144">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="3a622-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="3a622-145">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="3a622-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="3a622-146">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="3a622-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3a622-147">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="3a622-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="3a622-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3a622-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3a622-149">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3a622-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="3a622-150">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="3a622-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="3a622-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a622-151">RELATED LINKS</span></span>

