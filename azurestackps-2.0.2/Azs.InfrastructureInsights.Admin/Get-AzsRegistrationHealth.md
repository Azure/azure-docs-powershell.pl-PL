---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055672"
---
# <span data-ttu-id="6d703-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="6d703-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="6d703-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d703-102">SYNOPSIS</span></span>
<span data-ttu-id="6d703-103">Zwraca wymagane informacje dotyczące kondycji zasobu.</span><span class="sxs-lookup"><span data-stu-id="6d703-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="6d703-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d703-104">SYNTAX</span></span>

### <span data-ttu-id="6d703-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6d703-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d703-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="6d703-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d703-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d703-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6d703-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6d703-108">DESCRIPTION</span></span>
<span data-ttu-id="6d703-109">Zwraca wymagane informacje dotyczące kondycji zasobu.</span><span class="sxs-lookup"><span data-stu-id="6d703-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="6d703-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d703-110">EXAMPLES</span></span>

### <span data-ttu-id="6d703-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="6d703-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="6d703-112">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="6d703-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="6d703-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="6d703-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="6d703-114">Zwraca stan kondycji w obszarze a dla Microsoft. Fabric. Administrator.</span><span class="sxs-lookup"><span data-stu-id="6d703-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="6d703-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d703-115">PARAMETERS</span></span>

### <span data-ttu-id="6d703-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d703-116">-DefaultProfile</span></span>
<span data-ttu-id="6d703-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d703-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d703-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="6d703-118">-Filter</span></span>
<span data-ttu-id="6d703-119">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="6d703-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6d703-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6d703-120">-InputObject</span></span>
<span data-ttu-id="6d703-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6d703-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6d703-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6d703-122">-Location</span></span>
<span data-ttu-id="6d703-123">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="6d703-123">Name of the region</span></span>

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

### <span data-ttu-id="6d703-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d703-124">-ResourceGroupName</span></span>
<span data-ttu-id="6d703-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d703-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6d703-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="6d703-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="6d703-127">Identyfikator rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="6d703-127">Resource registration ID.</span></span>

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

### <span data-ttu-id="6d703-128">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="6d703-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="6d703-129">Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="6d703-129">Service registration ID.</span></span>

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

### <span data-ttu-id="6d703-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6d703-130">-SubscriptionId</span></span>
<span data-ttu-id="6d703-131">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d703-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d703-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6d703-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6d703-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d703-133">CommonParameters</span></span>
<span data-ttu-id="6d703-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d703-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d703-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d703-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d703-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d703-136">INPUTS</span></span>

### <span data-ttu-id="6d703-137">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6d703-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="6d703-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d703-138">OUTPUTS</span></span>

### <span data-ttu-id="6d703-139">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. Api20160501. IResourceHealth</span><span class="sxs-lookup"><span data-stu-id="6d703-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="6d703-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d703-140">NOTES</span></span>

<span data-ttu-id="6d703-141">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6d703-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d703-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d703-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6d703-143">INPUTobject <IInfrastructureInsightsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="6d703-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d703-144">`[AlertName <String>]`: Nazwa alertu.</span><span class="sxs-lookup"><span data-stu-id="6d703-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="6d703-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6d703-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d703-146">`[Location <String>]`: Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="6d703-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="6d703-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d703-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6d703-148">`[ResourceRegistrationId <String>]`: Identyfikator rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="6d703-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="6d703-149">`[ServiceHealth <String>]`: Nazwa kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="6d703-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="6d703-150">`[ServiceRegistrationId <String>]`: Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="6d703-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="6d703-151">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d703-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6d703-152">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6d703-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6d703-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d703-153">RELATED LINKS</span></span>

