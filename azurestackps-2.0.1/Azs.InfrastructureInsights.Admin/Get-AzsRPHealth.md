---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsrphealth
schema: 2.0.0
ms.openlocfilehash: 50b71b6804ea5d57e18fbbd2774c0ff9306a829d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054260"
---
# <span data-ttu-id="3e583-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="3e583-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="3e583-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e583-102">SYNOPSIS</span></span>
<span data-ttu-id="3e583-103">Zwraca żądany obiekt kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="3e583-103">Returns the requested service health object.</span></span>

## <span data-ttu-id="3e583-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e583-104">SYNTAX</span></span>

### <span data-ttu-id="3e583-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3e583-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e583-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3e583-106">Get</span></span>
```
Get-AzsRPHealth -ServiceHealth <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e583-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3e583-107">GetViaIdentity</span></span>
```
Get-AzsRPHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e583-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3e583-108">DESCRIPTION</span></span>
<span data-ttu-id="3e583-109">Zwraca żądany obiekt kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="3e583-109">Returns the requested service health object.</span></span>

## <span data-ttu-id="3e583-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e583-110">EXAMPLES</span></span>

### <span data-ttu-id="3e583-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="3e583-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRPHealth
```

<span data-ttu-id="3e583-112">Zwraca listę kondycji każdej usługi.</span><span class="sxs-lookup"><span data-stu-id="3e583-112">Returns a list of each service's health.</span></span>

### <span data-ttu-id="3e583-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="3e583-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="3e583-114">Zwraca wartość kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="3e583-114">Returns a service's health.</span></span>

## <span data-ttu-id="3e583-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e583-115">PARAMETERS</span></span>

### <span data-ttu-id="3e583-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e583-116">-DefaultProfile</span></span>
<span data-ttu-id="3e583-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e583-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e583-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="3e583-118">-Filter</span></span>
<span data-ttu-id="3e583-119">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="3e583-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e583-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3e583-120">-InputObject</span></span>
<span data-ttu-id="3e583-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3e583-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3e583-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3e583-122">-Location</span></span>
<span data-ttu-id="3e583-123">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="3e583-123">Name of the region</span></span>

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

### <span data-ttu-id="3e583-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e583-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e583-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e583-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e583-126">-Servicehealth</span><span class="sxs-lookup"><span data-stu-id="3e583-126">-ServiceHealth</span></span>
<span data-ttu-id="3e583-127">Nazwa kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="3e583-127">Service Health name.</span></span>

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

### <span data-ttu-id="3e583-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3e583-128">-SubscriptionId</span></span>
<span data-ttu-id="3e583-129">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e583-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e583-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3e583-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3e583-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e583-131">CommonParameters</span></span>
<span data-ttu-id="3e583-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e583-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e583-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e583-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e583-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e583-134">INPUTS</span></span>

### <span data-ttu-id="3e583-135">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3e583-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="3e583-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e583-136">OUTPUTS</span></span>

### <span data-ttu-id="3e583-137">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. Api20160501. IServiceHealth</span><span class="sxs-lookup"><span data-stu-id="3e583-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IServiceHealth</span></span>



## <span data-ttu-id="3e583-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e583-138">NOTES</span></span>

<span data-ttu-id="3e583-139">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3e583-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e583-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e583-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3e583-141">INPUTobject <IInfrastructureInsightsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3e583-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e583-142">`[AlertName <String>]`: Nazwa alertu.</span><span class="sxs-lookup"><span data-stu-id="3e583-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="3e583-143">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3e583-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e583-144">`[Location <String>]`: Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="3e583-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="3e583-145">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e583-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3e583-146">`[ResourceRegistrationId <String>]`: Identyfikator rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="3e583-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="3e583-147">`[ServiceHealth <String>]`: Nazwa kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="3e583-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="3e583-148">`[ServiceRegistrationId <String>]`: Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="3e583-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="3e583-149">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e583-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3e583-150">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3e583-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3e583-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e583-151">RELATED LINKS</span></span>

