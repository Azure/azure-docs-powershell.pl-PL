---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054188"
---
# <span data-ttu-id="d9d3b-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="d9d3b-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="d9d3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d3b-103">Zwraca wymagane informacje dotyczące kondycji zasobu.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="d9d3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9d3b-104">SYNTAX</span></span>

### <span data-ttu-id="d9d3b-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d9d3b-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9d3b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d9d3b-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9d3b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d9d3b-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d9d3b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d9d3b-108">DESCRIPTION</span></span>
<span data-ttu-id="d9d3b-109">Zwraca wymagane informacje dotyczące kondycji zasobu.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="d9d3b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9d3b-110">EXAMPLES</span></span>

### <span data-ttu-id="d9d3b-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="d9d3b-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="d9d3b-112">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="d9d3b-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="d9d3b-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="d9d3b-114">Zwraca stan kondycji w obszarze a dla Microsoft. Fabric. Administrator.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="d9d3b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9d3b-115">PARAMETERS</span></span>

### <span data-ttu-id="d9d3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d3b-116">-DefaultProfile</span></span>
<span data-ttu-id="d9d3b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9d3b-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="d9d3b-118">-Filter</span></span>
<span data-ttu-id="d9d3b-119">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="d9d3b-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d9d3b-120">-InputObject</span></span>
<span data-ttu-id="d9d3b-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d9d3b-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d9d3b-122">-Location</span></span>
<span data-ttu-id="d9d3b-123">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="d9d3b-123">Name of the region</span></span>

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

### <span data-ttu-id="d9d3b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d3b-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9d3b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="d9d3b-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="d9d3b-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="d9d3b-127">Identyfikator rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-127">Resource registration ID.</span></span>

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

### <span data-ttu-id="d9d3b-128">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="d9d3b-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="d9d3b-129">Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-129">Service registration ID.</span></span>

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

### <span data-ttu-id="d9d3b-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d9d3b-130">-SubscriptionId</span></span>
<span data-ttu-id="d9d3b-131">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9d3b-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d9d3b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d3b-133">CommonParameters</span></span>
<span data-ttu-id="d9d3b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d3b-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9d3b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d3b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9d3b-136">INPUTS</span></span>

### <span data-ttu-id="d9d3b-137">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d9d3b-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="d9d3b-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9d3b-138">OUTPUTS</span></span>

### <span data-ttu-id="d9d3b-139">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. Api20160501. IResourceHealth</span><span class="sxs-lookup"><span data-stu-id="d9d3b-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="d9d3b-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9d3b-140">NOTES</span></span>

<span data-ttu-id="d9d3b-141">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9d3b-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d9d3b-143">INPUTobject <IInfrastructureInsightsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d9d3b-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d9d3b-144">`[AlertName <String>]`: Nazwa alertu.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="d9d3b-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d9d3b-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d9d3b-146">`[Location <String>]`: Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="d9d3b-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="d9d3b-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d9d3b-148">`[ResourceRegistrationId <String>]`: Identyfikator rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="d9d3b-149">`[ServiceHealth <String>]`: Nazwa kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="d9d3b-150">`[ServiceRegistrationId <String>]`: Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="d9d3b-151">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d9d3b-152">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d9d3b-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d9d3b-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9d3b-153">RELATED LINKS</span></span>

