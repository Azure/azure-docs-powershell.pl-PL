---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055699"
---
# <span data-ttu-id="58190-101">Get-AzsLocation</span><span class="sxs-lookup"><span data-stu-id="58190-101">Get-AzsLocation</span></span>

## <span data-ttu-id="58190-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58190-102">SYNOPSIS</span></span>
<span data-ttu-id="58190-103">Pobierz określoną lokalizację.</span><span class="sxs-lookup"><span data-stu-id="58190-103">Get the specified location.</span></span>

## <span data-ttu-id="58190-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58190-104">SYNTAX</span></span>

### <span data-ttu-id="58190-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="58190-105">List (Default)</span></span>
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="58190-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="58190-106">Get</span></span>
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="58190-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="58190-107">GetViaIdentity</span></span>
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="58190-108">Opis</span><span class="sxs-lookup"><span data-stu-id="58190-108">DESCRIPTION</span></span>
<span data-ttu-id="58190-109">Pobierz określoną lokalizację.</span><span class="sxs-lookup"><span data-stu-id="58190-109">Get the specified location.</span></span>

## <span data-ttu-id="58190-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58190-110">EXAMPLES</span></span>

### <span data-ttu-id="58190-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58190-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

<span data-ttu-id="58190-112">Wyświetlanie listy wszystkich AzureStackych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="58190-112">Get a list of all AzureStack locations.</span></span>

## <span data-ttu-id="58190-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58190-113">PARAMETERS</span></span>

### <span data-ttu-id="58190-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58190-114">-DefaultProfile</span></span>
<span data-ttu-id="58190-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58190-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58190-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="58190-116">-InputObject</span></span>
<span data-ttu-id="58190-117">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="58190-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="58190-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58190-118">-Name</span></span>
<span data-ttu-id="58190-119">Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="58190-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="58190-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="58190-120">-SubscriptionId</span></span>
<span data-ttu-id="58190-121">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="58190-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="58190-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58190-122">CommonParameters</span></span>
<span data-ttu-id="58190-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58190-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58190-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58190-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58190-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58190-125">INPUTS</span></span>

### <span data-ttu-id="58190-126">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="58190-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="58190-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58190-127">OUTPUTS</span></span>

### <span data-ttu-id="58190-128">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. ILocation</span><span class="sxs-lookup"><span data-stu-id="58190-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ILocation</span></span>

<span data-ttu-id="58190-129">PISUJE</span><span class="sxs-lookup"><span data-stu-id="58190-129">ALIASES</span></span>

## <span data-ttu-id="58190-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58190-130">NOTES</span></span>

<span data-ttu-id="58190-131">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="58190-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="58190-132">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="58190-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="58190-133">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="58190-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="58190-134">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="58190-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="58190-135">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="58190-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="58190-136">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="58190-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="58190-137">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="58190-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="58190-138">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="58190-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="58190-139">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="58190-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="58190-140">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="58190-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="58190-141">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="58190-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="58190-142">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="58190-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="58190-143">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="58190-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="58190-144">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="58190-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="58190-145">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="58190-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="58190-146">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="58190-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="58190-147">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="58190-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="58190-148">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="58190-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="58190-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58190-149">RELATED LINKS</span></span>

