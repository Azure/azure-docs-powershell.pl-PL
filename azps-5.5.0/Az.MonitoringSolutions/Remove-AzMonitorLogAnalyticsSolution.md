---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187338"
---
# <span data-ttu-id="9f395-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="9f395-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="9f395-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f395-102">SYNOPSIS</span></span>
<span data-ttu-id="9f395-103">Usuwa rozwiązanie z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9f395-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="9f395-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9f395-104">SYNTAX</span></span>

### <span data-ttu-id="9f395-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="9f395-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9f395-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9f395-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f395-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9f395-107">DESCRIPTION</span></span>
<span data-ttu-id="9f395-108">Usuwa rozwiązanie z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9f395-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="9f395-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9f395-109">EXAMPLES</span></span>

### <span data-ttu-id="9f395-110">Przykład 1. Usuwanie rozwiązania do analizy dzienników monitorów według nazwy</span><span class="sxs-lookup"><span data-stu-id="9f395-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="9f395-111">To polecenie usuwa rozwiązanie do analizy dzienników monitorów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="9f395-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="9f395-112">Przykład 2. Usuwanie rozwiązania analizy dziennika monitora według obiektu</span><span class="sxs-lookup"><span data-stu-id="9f395-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="9f395-113">To polecenie usuwa obiektowe rozwiązanie do analizy dziennika monitorów.</span><span class="sxs-lookup"><span data-stu-id="9f395-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="9f395-114">Przykład 3. Usuwanie rozwiązania analizy dziennika monitora według potoku</span><span class="sxs-lookup"><span data-stu-id="9f395-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="9f395-115">To polecenie usuwa rozwiązanie do analizy dzienników monitorów według potoku.</span><span class="sxs-lookup"><span data-stu-id="9f395-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="9f395-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f395-116">PARAMETERS</span></span>

### <span data-ttu-id="9f395-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f395-117">-DefaultProfile</span></span>
<span data-ttu-id="9f395-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f395-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f395-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f395-119">-InputObject</span></span>
<span data-ttu-id="9f395-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9f395-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f395-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9f395-121">-Name</span></span>
<span data-ttu-id="9f395-122">Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9f395-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f395-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f395-123">-PassThru</span></span>
<span data-ttu-id="9f395-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9f395-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f395-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f395-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f395-126">Nazwa grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="9f395-126">The name of the resource group to get.</span></span>
<span data-ttu-id="9f395-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9f395-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f395-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f395-128">-SubscriptionId</span></span>
<span data-ttu-id="9f395-129">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f395-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9f395-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="9f395-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f395-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f395-131">-Confirm</span></span>
<span data-ttu-id="9f395-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9f395-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f395-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f395-133">-WhatIf</span></span>
<span data-ttu-id="9f395-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f395-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f395-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9f395-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f395-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f395-136">CommonParameters</span></span>
<span data-ttu-id="9f395-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f395-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f395-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f395-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f395-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f395-139">INPUTS</span></span>

### <span data-ttu-id="9f395-140">Microsoft.Azure.PowerShell.Cmdlet.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="9f395-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="9f395-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f395-141">OUTPUTS</span></span>

### <span data-ttu-id="9f395-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f395-142">System.Boolean</span></span>

## <span data-ttu-id="9f395-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9f395-143">NOTES</span></span>

<span data-ttu-id="9f395-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9f395-144">ALIASES</span></span>

<span data-ttu-id="9f395-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f395-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f395-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9f395-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f395-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9f395-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f395-148">INPUTOBJECT: <IMonitoringSolutionsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="9f395-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9f395-149">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9f395-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9f395-150">`[ManagementAssociationName <String>]`: Nazwa skojarzenia zarządzania użytkownikami.</span><span class="sxs-lookup"><span data-stu-id="9f395-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="9f395-151">`[ManagementConfigurationName <String>]`: nazwa konfiguracji zarządzania użytkownikami.</span><span class="sxs-lookup"><span data-stu-id="9f395-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="9f395-152">`[ProviderName <String>]`: nazwa dostawcy dla zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="9f395-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="9f395-153">`[ResourceGroupName <String>]`: nazwa grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="9f395-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="9f395-154">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9f395-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="9f395-155">`[ResourceName <String>]`: nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="9f395-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="9f395-156">`[ResourceType <String>]`: typ zasobu nadrzędnego</span><span class="sxs-lookup"><span data-stu-id="9f395-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="9f395-157">`[SolutionName <String>]`: nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9f395-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="9f395-158">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f395-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9f395-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="9f395-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9f395-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f395-160">RELATED LINKS</span></span>

