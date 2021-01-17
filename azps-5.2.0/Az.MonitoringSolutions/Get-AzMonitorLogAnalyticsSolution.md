---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353005"
---
# <span data-ttu-id="7680b-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="7680b-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="7680b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7680b-102">SYNOPSIS</span></span>
<span data-ttu-id="7680b-103">Pobiera rozwiązanie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7680b-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="7680b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7680b-104">SYNTAX</span></span>

### <span data-ttu-id="7680b-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7680b-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7680b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="7680b-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7680b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7680b-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7680b-108">Lista</span><span class="sxs-lookup"><span data-stu-id="7680b-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7680b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7680b-109">DESCRIPTION</span></span>
<span data-ttu-id="7680b-110">Pobiera rozwiązanie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7680b-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="7680b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7680b-111">EXAMPLES</span></span>

### <span data-ttu-id="7680b-112">Przykład 1: Uzyskaj rozwiązanie analizy dziennika monitora według nazwy</span><span class="sxs-lookup"><span data-stu-id="7680b-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="7680b-113">To polecenie pobiera rozwiązanie analizy dzienników według nazwy.</span><span class="sxs-lookup"><span data-stu-id="7680b-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="7680b-114">Przykład 2: uzyskiwanie rozwiązania analiza dziennika monitora według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="7680b-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="7680b-115">To polecenie pobiera rozwiązanie analizy dzienników według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="7680b-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="7680b-116">Przykład 3: uzyskiwanie rozwiązania analiza dziennika monitora według obiektu</span><span class="sxs-lookup"><span data-stu-id="7680b-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="7680b-117">To polecenie pobiera rozwiązanie analizy dziennika według obiektu.</span><span class="sxs-lookup"><span data-stu-id="7680b-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="7680b-118">Przykład 4: pobieranie wszystkich rozwiązań analizy dzienników na monitorze w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="7680b-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="7680b-119">To polecenie pobiera wszystkie rozwiązania analizy dzienników w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7680b-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="7680b-120">Przykład 5: pobieranie wszystkich rozwiązań analizy dzienników na monitorze w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="7680b-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="7680b-121">To polecenie pobiera wszystkie rozwiązania analizy dzienników w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7680b-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="7680b-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7680b-122">PARAMETERS</span></span>

### <span data-ttu-id="7680b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7680b-123">-DefaultProfile</span></span>
<span data-ttu-id="7680b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7680b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7680b-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7680b-125">-InputObject</span></span>
<span data-ttu-id="7680b-126">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7680b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7680b-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7680b-127">-Name</span></span>
<span data-ttu-id="7680b-128">Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7680b-128">User Solution Name.</span></span>

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

### <span data-ttu-id="7680b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7680b-129">-ResourceGroupName</span></span>
<span data-ttu-id="7680b-130">Nazwa grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="7680b-130">The name of the resource group to get.</span></span>
<span data-ttu-id="7680b-131">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="7680b-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7680b-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7680b-132">-SubscriptionId</span></span>
<span data-ttu-id="7680b-133">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7680b-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7680b-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7680b-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7680b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7680b-135">CommonParameters</span></span>
<span data-ttu-id="7680b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7680b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7680b-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7680b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7680b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7680b-138">INPUTS</span></span>

### <span data-ttu-id="7680b-139">Microsoft. Azure. PowerShell. polecenia. MonitoringSolutions. models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="7680b-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="7680b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7680b-140">OUTPUTS</span></span>

### <span data-ttu-id="7680b-141">Microsoft. Azure. PowerShell. polecenia. MonitoringSolutions. models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="7680b-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="7680b-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7680b-142">NOTES</span></span>

<span data-ttu-id="7680b-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7680b-143">ALIASES</span></span>

<span data-ttu-id="7680b-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7680b-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7680b-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7680b-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7680b-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7680b-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7680b-147">INPUTobject <IMonitoringSolutionsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7680b-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7680b-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7680b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7680b-149">`[ManagementAssociationName <String>]`: Nazwa użytkownika ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="7680b-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="7680b-150">`[ManagementConfigurationName <String>]`: Nazwa konfiguracji zarządzania użytkownikami.</span><span class="sxs-lookup"><span data-stu-id="7680b-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="7680b-151">`[ProviderName <String>]`: Nazwa dostawcy dla zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="7680b-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="7680b-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="7680b-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="7680b-153">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="7680b-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="7680b-154">`[ResourceName <String>]`: Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="7680b-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="7680b-155">`[ResourceType <String>]`: Typ zasobu dla zasobu nadrzędnego</span><span class="sxs-lookup"><span data-stu-id="7680b-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="7680b-156">`[SolutionName <String>]`: Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7680b-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="7680b-157">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7680b-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7680b-158">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7680b-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7680b-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7680b-159">RELATED LINKS</span></span>

