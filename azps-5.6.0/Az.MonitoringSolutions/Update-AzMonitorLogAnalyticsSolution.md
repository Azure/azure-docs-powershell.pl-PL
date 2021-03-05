---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: e1c1181dc81d5d15fbaed02fa255961cefe2ae28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984467"
---
# <span data-ttu-id="433e5-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="433e5-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="433e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="433e5-102">SYNOPSIS</span></span>
<span data-ttu-id="433e5-103">Aktualizowanie tagów rozwiązania.</span><span class="sxs-lookup"><span data-stu-id="433e5-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="433e5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="433e5-104">SYNTAX</span></span>

### <span data-ttu-id="433e5-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="433e5-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="433e5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="433e5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="433e5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="433e5-107">DESCRIPTION</span></span>
<span data-ttu-id="433e5-108">Aktualizowanie tagów rozwiązania.</span><span class="sxs-lookup"><span data-stu-id="433e5-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="433e5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="433e5-109">EXAMPLES</span></span>

### <span data-ttu-id="433e5-110">Przykład 1. Aktualizowanie rozwiązania analizy dziennika monitora według nazwy</span><span class="sxs-lookup"><span data-stu-id="433e5-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="433e5-111">To polecenie aktualizuje rozwiązanie do analizy dzienników monitorów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="433e5-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="433e5-112">Przykład 2. Aktualizowanie rozwiązania analizy dziennika monitora według obiektu</span><span class="sxs-lookup"><span data-stu-id="433e5-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="433e5-113">To polecenie aktualizuje rozwiązanie analizy dziennika monitorów według obiektów.</span><span class="sxs-lookup"><span data-stu-id="433e5-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="433e5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="433e5-114">PARAMETERS</span></span>

### <span data-ttu-id="433e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433e5-115">-DefaultProfile</span></span>
<span data-ttu-id="433e5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="433e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433e5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="433e5-117">-InputObject</span></span>
<span data-ttu-id="433e5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="433e5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="433e5-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="433e5-119">-Name</span></span>
<span data-ttu-id="433e5-120">Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="433e5-120">User Solution Name.</span></span>

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

### <span data-ttu-id="433e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="433e5-122">Nazwa grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="433e5-122">The name of the resource group to get.</span></span>
<span data-ttu-id="433e5-123">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="433e5-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="433e5-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="433e5-124">-SubscriptionId</span></span>
<span data-ttu-id="433e5-125">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="433e5-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="433e5-126">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="433e5-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="433e5-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="433e5-127">-Tag</span></span>
<span data-ttu-id="433e5-128">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="433e5-128">Resource tags</span></span>

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

### <span data-ttu-id="433e5-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="433e5-129">-Confirm</span></span>
<span data-ttu-id="433e5-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="433e5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="433e5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="433e5-131">-WhatIf</span></span>
<span data-ttu-id="433e5-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="433e5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="433e5-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="433e5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="433e5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433e5-134">CommonParameters</span></span>
<span data-ttu-id="433e5-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433e5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433e5-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="433e5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433e5-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="433e5-137">INPUTS</span></span>

### <span data-ttu-id="433e5-138">Microsoft.Azure.PowerShell.Cmdlet.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="433e5-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="433e5-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="433e5-139">OUTPUTS</span></span>

### <span data-ttu-id="433e5-140">Microsoft.Azure.PowerShell.Cmdlet.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="433e5-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="433e5-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="433e5-141">NOTES</span></span>

<span data-ttu-id="433e5-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="433e5-142">ALIASES</span></span>

<span data-ttu-id="433e5-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="433e5-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="433e5-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="433e5-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="433e5-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="433e5-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="433e5-146">INPUTOBJECT: <IMonitoringSolutionsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="433e5-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="433e5-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="433e5-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="433e5-148">`[ManagementAssociationName <String>]`: Nazwa skojarzenia zarządzania użytkownikami.</span><span class="sxs-lookup"><span data-stu-id="433e5-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="433e5-149">`[ManagementConfigurationName <String>]`: nazwa konfiguracji zarządzania użytkownikami.</span><span class="sxs-lookup"><span data-stu-id="433e5-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="433e5-150">`[ProviderName <String>]`: nazwa dostawcy dla zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="433e5-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="433e5-151">`[ResourceGroupName <String>]`: nazwa grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="433e5-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="433e5-152">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="433e5-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="433e5-153">`[ResourceName <String>]`: nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="433e5-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="433e5-154">`[ResourceType <String>]`: typ zasobu nadrzędnego</span><span class="sxs-lookup"><span data-stu-id="433e5-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="433e5-155">`[SolutionName <String>]`: nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="433e5-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="433e5-156">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="433e5-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="433e5-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="433e5-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="433e5-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="433e5-158">RELATED LINKS</span></span>

