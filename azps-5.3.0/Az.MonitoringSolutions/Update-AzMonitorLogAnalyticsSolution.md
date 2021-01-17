---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490077"
---
# <span data-ttu-id="66a35-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="66a35-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="66a35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66a35-102">SYNOPSIS</span></span>
<span data-ttu-id="66a35-103">Zaktualizuj znaczniki rozwiązania.</span><span class="sxs-lookup"><span data-stu-id="66a35-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="66a35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66a35-104">SYNTAX</span></span>

### <span data-ttu-id="66a35-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="66a35-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="66a35-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="66a35-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="66a35-107">Opis</span><span class="sxs-lookup"><span data-stu-id="66a35-107">DESCRIPTION</span></span>
<span data-ttu-id="66a35-108">Zaktualizuj znaczniki rozwiązania.</span><span class="sxs-lookup"><span data-stu-id="66a35-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="66a35-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66a35-109">EXAMPLES</span></span>

### <span data-ttu-id="66a35-110">Przykład 1: aktualizowanie rozwiązania analizy dziennika monitora według nazwy</span><span class="sxs-lookup"><span data-stu-id="66a35-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="66a35-111">To polecenie aktualizuje rozwiązanie analizy dzienników według nazwy.</span><span class="sxs-lookup"><span data-stu-id="66a35-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="66a35-112">Przykład 2: aktualizowanie rozwiązania analizy dziennika monitora według obiektów</span><span class="sxs-lookup"><span data-stu-id="66a35-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="66a35-113">To polecenie aktualizuje rozwiązanie analizy dziennika według obiektu.</span><span class="sxs-lookup"><span data-stu-id="66a35-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="66a35-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66a35-114">PARAMETERS</span></span>

### <span data-ttu-id="66a35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a35-115">-DefaultProfile</span></span>
<span data-ttu-id="66a35-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66a35-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a35-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66a35-117">-InputObject</span></span>
<span data-ttu-id="66a35-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="66a35-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66a35-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66a35-119">-Name</span></span>
<span data-ttu-id="66a35-120">Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="66a35-120">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a35-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a35-121">-ResourceGroupName</span></span>
<span data-ttu-id="66a35-122">Nazwa grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="66a35-122">The name of the resource group to get.</span></span>
<span data-ttu-id="66a35-123">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="66a35-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a35-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="66a35-124">-SubscriptionId</span></span>
<span data-ttu-id="66a35-125">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="66a35-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="66a35-126">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="66a35-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a35-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="66a35-127">-Tag</span></span>
<span data-ttu-id="66a35-128">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="66a35-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a35-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66a35-129">-Confirm</span></span>
<span data-ttu-id="66a35-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a35-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a35-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a35-131">-WhatIf</span></span>
<span data-ttu-id="66a35-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a35-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a35-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="66a35-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a35-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a35-134">CommonParameters</span></span>
<span data-ttu-id="66a35-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a35-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a35-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66a35-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a35-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66a35-137">INPUTS</span></span>

### <span data-ttu-id="66a35-138">Microsoft. Azure. PowerShell. polecenia. MonitoringSolutions. models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="66a35-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="66a35-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66a35-139">OUTPUTS</span></span>

### <span data-ttu-id="66a35-140">Microsoft. Azure. PowerShell. polecenia. MonitoringSolutions. models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="66a35-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="66a35-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66a35-141">NOTES</span></span>

<span data-ttu-id="66a35-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="66a35-142">ALIASES</span></span>

<span data-ttu-id="66a35-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66a35-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="66a35-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="66a35-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66a35-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66a35-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="66a35-146">INPUTobject <IMonitoringSolutionsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="66a35-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66a35-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="66a35-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66a35-148">`[ManagementAssociationName <String>]`: Nazwa użytkownika ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="66a35-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="66a35-149">`[ManagementConfigurationName <String>]`: Nazwa konfiguracji zarządzania użytkownikami.</span><span class="sxs-lookup"><span data-stu-id="66a35-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="66a35-150">`[ProviderName <String>]`: Nazwa dostawcy dla zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="66a35-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="66a35-151">`[ResourceGroupName <String>]`: Nazwa grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="66a35-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="66a35-152">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="66a35-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="66a35-153">`[ResourceName <String>]`: Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="66a35-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="66a35-154">`[ResourceType <String>]`: Typ zasobu dla zasobu nadrzędnego</span><span class="sxs-lookup"><span data-stu-id="66a35-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="66a35-155">`[SolutionName <String>]`: Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="66a35-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="66a35-156">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="66a35-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="66a35-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="66a35-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="66a35-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66a35-158">RELATED LINKS</span></span>

