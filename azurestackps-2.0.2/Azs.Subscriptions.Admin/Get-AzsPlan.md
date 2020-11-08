---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplan
schema: 2.0.0
ms.openlocfilehash: 4aa59d41bc13d79e487465a6a0721ec19ed68bb8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055962"
---
# <span data-ttu-id="57a5a-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="57a5a-101">Get-AzsPlan</span></span>

## <span data-ttu-id="57a5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="57a5a-103">Pobierz określony plan.</span><span class="sxs-lookup"><span data-stu-id="57a5a-103">Get the specified plan.</span></span>

## <span data-ttu-id="57a5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57a5a-104">SYNTAX</span></span>

### <span data-ttu-id="57a5a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="57a5a-105">List (Default)</span></span>
```
Get-AzsPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57a5a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="57a5a-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57a5a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57a5a-107">GetViaIdentity</span></span>
```
Get-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57a5a-108">List1</span><span class="sxs-lookup"><span data-stu-id="57a5a-108">List1</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="57a5a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="57a5a-109">DESCRIPTION</span></span>
<span data-ttu-id="57a5a-110">Pobierz określony plan.</span><span class="sxs-lookup"><span data-stu-id="57a5a-110">Get the specified plan.</span></span>

## <span data-ttu-id="57a5a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57a5a-111">EXAMPLES</span></span>

### <span data-ttu-id="57a5a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57a5a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 1
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="57a5a-113">Pobierz plan konkretną w ramach tych abonamentów.</span><span class="sxs-lookup"><span data-stu-id="57a5a-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="57a5a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57a5a-114">PARAMETERS</span></span>

### <span data-ttu-id="57a5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a5a-115">-DefaultProfile</span></span>
<span data-ttu-id="57a5a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57a5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57a5a-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="57a5a-117">-InputObject</span></span>
<span data-ttu-id="57a5a-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="57a5a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57a5a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57a5a-119">-Name</span></span>
<span data-ttu-id="57a5a-120">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="57a5a-120">Name of the plan.</span></span>

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

### <span data-ttu-id="57a5a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a5a-121">-ResourceGroupName</span></span>
<span data-ttu-id="57a5a-122">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="57a5a-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="57a5a-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="57a5a-123">-SubscriptionId</span></span>
<span data-ttu-id="57a5a-124">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="57a5a-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="57a5a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a5a-125">CommonParameters</span></span>
<span data-ttu-id="57a5a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a5a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a5a-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57a5a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a5a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57a5a-128">INPUTS</span></span>

### <span data-ttu-id="57a5a-129">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="57a5a-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="57a5a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57a5a-130">OUTPUTS</span></span>

### <span data-ttu-id="57a5a-131">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="57a5a-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="57a5a-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="57a5a-132">ALIASES</span></span>

## <span data-ttu-id="57a5a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57a5a-133">NOTES</span></span>

<span data-ttu-id="57a5a-134">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="57a5a-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57a5a-135">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57a5a-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="57a5a-136">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="57a5a-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57a5a-137">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="57a5a-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="57a5a-138">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="57a5a-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="57a5a-139">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="57a5a-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57a5a-140">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="57a5a-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="57a5a-141">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="57a5a-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="57a5a-142">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="57a5a-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="57a5a-143">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="57a5a-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="57a5a-144">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="57a5a-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="57a5a-145">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="57a5a-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="57a5a-146">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="57a5a-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="57a5a-147">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="57a5a-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="57a5a-148">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="57a5a-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="57a5a-149">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="57a5a-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="57a5a-150">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="57a5a-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="57a5a-151">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="57a5a-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="57a5a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57a5a-152">RELATED LINKS</span></span>

