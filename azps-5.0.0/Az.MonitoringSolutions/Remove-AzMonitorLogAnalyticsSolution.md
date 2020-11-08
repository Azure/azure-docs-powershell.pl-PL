---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233871"
---
# <span data-ttu-id="d46a9-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="d46a9-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="d46a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d46a9-102">SYNOPSIS</span></span>
<span data-ttu-id="d46a9-103">Usuwa rozwiązanie w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d46a9-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="d46a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d46a9-104">SYNTAX</span></span>

### <span data-ttu-id="d46a9-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d46a9-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d46a9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d46a9-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d46a9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d46a9-107">DESCRIPTION</span></span>
<span data-ttu-id="d46a9-108">Usuwa rozwiązanie w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d46a9-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="d46a9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d46a9-109">EXAMPLES</span></span>

### <span data-ttu-id="d46a9-110">Przykład 1: usuwanie rozwiązania analizy dziennika monitora według nazwy</span><span class="sxs-lookup"><span data-stu-id="d46a9-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="d46a9-111">To polecenie usuwa rozwiązanie analizy dziennika monitora według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d46a9-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="d46a9-112">Przykład 2: usuwanie rozwiązania analizy dziennika monitorowania według obiektów</span><span class="sxs-lookup"><span data-stu-id="d46a9-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="d46a9-113">To polecenie usuwa rozwiązanie analiza dziennika monitorowania według obiektu.</span><span class="sxs-lookup"><span data-stu-id="d46a9-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="d46a9-114">Przykład 3: usuwanie rozwiązania analizy dzienników według rurociągu</span><span class="sxs-lookup"><span data-stu-id="d46a9-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="d46a9-115">To polecenie umożliwia usunięcie rozwiązania analizy dziennika monitora według rurociągu.</span><span class="sxs-lookup"><span data-stu-id="d46a9-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="d46a9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d46a9-116">PARAMETERS</span></span>

### <span data-ttu-id="d46a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46a9-117">-DefaultProfile</span></span>
<span data-ttu-id="d46a9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d46a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d46a9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d46a9-119">-InputObject</span></span>
<span data-ttu-id="d46a9-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d46a9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d46a9-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d46a9-121">-Name</span></span>
<span data-ttu-id="d46a9-122">Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d46a9-122">User Solution Name.</span></span>

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

### <span data-ttu-id="d46a9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d46a9-123">-PassThru</span></span>
<span data-ttu-id="d46a9-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="d46a9-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d46a9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d46a9-125">-ResourceGroupName</span></span>
<span data-ttu-id="d46a9-126">Nazwa grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="d46a9-126">The name of the resource group to get.</span></span>
<span data-ttu-id="d46a9-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="d46a9-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d46a9-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d46a9-128">-SubscriptionId</span></span>
<span data-ttu-id="d46a9-129">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d46a9-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d46a9-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d46a9-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d46a9-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d46a9-131">-Confirm</span></span>
<span data-ttu-id="d46a9-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46a9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d46a9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46a9-133">-WhatIf</span></span>
<span data-ttu-id="d46a9-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46a9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46a9-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d46a9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d46a9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46a9-136">CommonParameters</span></span>
<span data-ttu-id="d46a9-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46a9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46a9-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d46a9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46a9-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d46a9-139">INPUTS</span></span>

### <span data-ttu-id="d46a9-140">Microsoft. Azure. PowerShell. polecenia. MonitoringSolutions. models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="d46a9-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="d46a9-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d46a9-141">OUTPUTS</span></span>

### <span data-ttu-id="d46a9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d46a9-142">System.Boolean</span></span>

## <span data-ttu-id="d46a9-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d46a9-143">NOTES</span></span>

<span data-ttu-id="d46a9-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d46a9-144">ALIASES</span></span>

<span data-ttu-id="d46a9-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d46a9-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d46a9-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d46a9-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d46a9-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d46a9-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d46a9-148">INPUTobject <IMonitoringSolutionsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d46a9-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d46a9-149">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d46a9-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d46a9-150">`[ManagementAssociationName <String>]`: Nazwa użytkownika ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="d46a9-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="d46a9-151">`[ManagementConfigurationName <String>]`: Nazwa konfiguracji zarządzania użytkownikami.</span><span class="sxs-lookup"><span data-stu-id="d46a9-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="d46a9-152">`[ProviderName <String>]`: Nazwa dostawcy dla zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="d46a9-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="d46a9-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="d46a9-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="d46a9-154">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="d46a9-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="d46a9-155">`[ResourceName <String>]`: Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="d46a9-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="d46a9-156">`[ResourceType <String>]`: Typ zasobu dla zasobu nadrzędnego</span><span class="sxs-lookup"><span data-stu-id="d46a9-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="d46a9-157">`[SolutionName <String>]`: Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d46a9-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="d46a9-158">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d46a9-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d46a9-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="d46a9-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d46a9-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d46a9-160">RELATED LINKS</span></span>

