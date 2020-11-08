---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsalert
schema: 2.0.0
ms.openlocfilehash: 097793edf89bed5193ef007b6bad0803a9082149
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054264"
---
# <span data-ttu-id="2e66d-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="2e66d-101">Get-AzsAlert</span></span>

## <span data-ttu-id="2e66d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e66d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e66d-103">Zwraca żądany alert.</span><span class="sxs-lookup"><span data-stu-id="2e66d-103">Returns the requested alert.</span></span>

## <span data-ttu-id="2e66d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e66d-104">SYNTAX</span></span>

### <span data-ttu-id="2e66d-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2e66d-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e66d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2e66d-106">Get</span></span>
```
Get-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e66d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2e66d-107">GetViaIdentity</span></span>
```
Get-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e66d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2e66d-108">DESCRIPTION</span></span>
<span data-ttu-id="2e66d-109">Zwraca żądany alert.</span><span class="sxs-lookup"><span data-stu-id="2e66d-109">Returns the requested alert.</span></span>

## <span data-ttu-id="2e66d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e66d-110">EXAMPLES</span></span>

### <span data-ttu-id="2e66d-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="2e66d-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="2e66d-112">Uzyskaj alert według nazwy.</span><span class="sxs-lookup"><span data-stu-id="2e66d-112">Get an alert by Name.</span></span>

### <span data-ttu-id="2e66d-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="2e66d-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="2e66d-114">Pobieranie wszystkich aktywnych alertów i wyświetlanie ich usterek i tytułów.</span><span class="sxs-lookup"><span data-stu-id="2e66d-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="2e66d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e66d-115">PARAMETERS</span></span>

### <span data-ttu-id="2e66d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e66d-116">-DefaultProfile</span></span>
<span data-ttu-id="2e66d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e66d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e66d-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="2e66d-118">-Filter</span></span>
<span data-ttu-id="2e66d-119">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="2e66d-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="2e66d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e66d-120">-InputObject</span></span>
<span data-ttu-id="2e66d-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2e66d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2e66d-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2e66d-122">-Location</span></span>
<span data-ttu-id="2e66d-123">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="2e66d-123">Name of the region</span></span>

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

### <span data-ttu-id="2e66d-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e66d-124">-Name</span></span>
<span data-ttu-id="2e66d-125">Nazwa alertu.</span><span class="sxs-lookup"><span data-stu-id="2e66d-125">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2e66d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e66d-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e66d-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e66d-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="2e66d-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2e66d-128">-SubscriptionId</span></span>
<span data-ttu-id="2e66d-129">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2e66d-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2e66d-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2e66d-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2e66d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e66d-131">CommonParameters</span></span>
<span data-ttu-id="2e66d-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e66d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e66d-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e66d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e66d-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e66d-134">INPUTS</span></span>

### <span data-ttu-id="2e66d-135">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2e66d-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="2e66d-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e66d-136">OUTPUTS</span></span>

### <span data-ttu-id="2e66d-137">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="2e66d-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="2e66d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e66d-138">NOTES</span></span>

<span data-ttu-id="2e66d-139">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2e66d-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e66d-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e66d-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2e66d-141">INPUTobject <IInfrastructureInsightsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2e66d-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e66d-142">`[AlertName <String>]`: Nazwa alertu.</span><span class="sxs-lookup"><span data-stu-id="2e66d-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="2e66d-143">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2e66d-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e66d-144">`[Location <String>]`: Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="2e66d-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="2e66d-145">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e66d-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2e66d-146">`[ResourceRegistrationId <String>]`: Identyfikator rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="2e66d-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="2e66d-147">`[ServiceHealth <String>]`: Nazwa kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="2e66d-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="2e66d-148">`[ServiceRegistrationId <String>]`: Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="2e66d-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="2e66d-149">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2e66d-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2e66d-150">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2e66d-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2e66d-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e66d-151">RELATED LINKS</span></span>

