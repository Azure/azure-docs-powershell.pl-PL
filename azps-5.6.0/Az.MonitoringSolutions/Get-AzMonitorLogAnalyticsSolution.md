---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: f4be2a5da2dc8455b6e6674e7e74050ea506ae0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984502"
---
# <span data-ttu-id="e3975-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="e3975-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="e3975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3975-102">SYNOPSIS</span></span>
<span data-ttu-id="e3975-103">Pobiera rozwiązanie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3975-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="e3975-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e3975-104">SYNTAX</span></span>

### <span data-ttu-id="e3975-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e3975-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3975-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e3975-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3975-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3975-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3975-108">Lista</span><span class="sxs-lookup"><span data-stu-id="e3975-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e3975-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e3975-109">DESCRIPTION</span></span>
<span data-ttu-id="e3975-110">Pobiera rozwiązanie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3975-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="e3975-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e3975-111">EXAMPLES</span></span>

### <span data-ttu-id="e3975-112">Przykład 1. Uzyskiwanie rozwiązania do analizy dzienników monitorów według nazwy</span><span class="sxs-lookup"><span data-stu-id="e3975-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e3975-113">To polecenie otrzymuje rozwiązanie do analizy dzienników monitorów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="e3975-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="e3975-114">Przykład 2. Uzyskiwanie rozwiązania do analizy dziennika monitorów według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="e3975-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="e3975-115">To polecenie pobiera rozwiązanie do analizy dziennika monitorów według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="e3975-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="e3975-116">Przykład 3. Uzyskiwanie rozwiązania do analizy dziennika monitorów według obiektów</span><span class="sxs-lookup"><span data-stu-id="e3975-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e3975-117">To polecenie pobiera obiektowe rozwiązanie do analizy dziennika monitorów.</span><span class="sxs-lookup"><span data-stu-id="e3975-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="e3975-118">Przykład 4. Uzyskiwanie wszystkich rozwiązań do analizy dziennika monitorów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="e3975-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e3975-119">To polecenie pobiera wszystkie rozwiązania analizy dziennika monitorowania w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e3975-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="e3975-120">Przykład 5. Uzyskiwanie wszystkich rozwiązań do analizy dzienników monitorów w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e3975-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e3975-121">To polecenie pobiera wszystkie rozwiązania analizy dziennika monitorów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e3975-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="e3975-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3975-122">PARAMETERS</span></span>

### <span data-ttu-id="e3975-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3975-123">-DefaultProfile</span></span>
<span data-ttu-id="e3975-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3975-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3975-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3975-125">-InputObject</span></span>
<span data-ttu-id="e3975-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e3975-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3975-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e3975-127">-Name</span></span>
<span data-ttu-id="e3975-128">Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3975-128">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3975-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3975-129">-ResourceGroupName</span></span>
<span data-ttu-id="e3975-130">Nazwa grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="e3975-130">The name of the resource group to get.</span></span>
<span data-ttu-id="e3975-131">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e3975-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e3975-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3975-132">-SubscriptionId</span></span>
<span data-ttu-id="e3975-133">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e3975-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e3975-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="e3975-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e3975-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3975-135">CommonParameters</span></span>
<span data-ttu-id="e3975-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3975-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3975-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3975-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3975-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3975-138">INPUTS</span></span>

### <span data-ttu-id="e3975-139">Microsoft.Azure.PowerShell.Cmdlet.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="e3975-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="e3975-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3975-140">OUTPUTS</span></span>

### <span data-ttu-id="e3975-141">Microsoft.Azure.PowerShell.Cmdlet.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="e3975-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="e3975-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e3975-142">NOTES</span></span>

<span data-ttu-id="e3975-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e3975-143">ALIASES</span></span>

<span data-ttu-id="e3975-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3975-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3975-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e3975-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3975-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3975-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3975-147">INPUTOBJECT: <IMonitoringSolutionsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e3975-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3975-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e3975-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3975-149">`[ManagementAssociationName <String>]`: Nazwa skojarzenia zarządzania użytkownikami.</span><span class="sxs-lookup"><span data-stu-id="e3975-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="e3975-150">`[ManagementConfigurationName <String>]`: nazwa konfiguracji zarządzania użytkownikami.</span><span class="sxs-lookup"><span data-stu-id="e3975-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="e3975-151">`[ProviderName <String>]`: nazwa dostawcy dla zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="e3975-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="e3975-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="e3975-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="e3975-153">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e3975-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="e3975-154">`[ResourceName <String>]`: nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="e3975-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="e3975-155">`[ResourceType <String>]`: typ zasobu nadrzędnego</span><span class="sxs-lookup"><span data-stu-id="e3975-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="e3975-156">`[SolutionName <String>]`: nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3975-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="e3975-157">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e3975-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e3975-158">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="e3975-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e3975-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3975-159">RELATED LINKS</span></span>

