---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344542"
---
# <span data-ttu-id="84d93-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="84d93-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="84d93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84d93-102">SYNOPSIS</span></span>
<span data-ttu-id="84d93-103">Usuwa rozwiązanie w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="84d93-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="84d93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84d93-104">SYNTAX</span></span>

### <span data-ttu-id="84d93-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="84d93-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="84d93-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="84d93-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84d93-107">Opis</span><span class="sxs-lookup"><span data-stu-id="84d93-107">DESCRIPTION</span></span>
<span data-ttu-id="84d93-108">Usuwa rozwiązanie w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="84d93-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="84d93-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84d93-109">EXAMPLES</span></span>

### <span data-ttu-id="84d93-110">Przykład 1: usuwanie rozwiązania analizy dziennika monitora według nazwy</span><span class="sxs-lookup"><span data-stu-id="84d93-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="84d93-111">To polecenie usuwa rozwiązanie analizy dziennika monitora według nazwy.</span><span class="sxs-lookup"><span data-stu-id="84d93-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="84d93-112">Przykład 2: usuwanie rozwiązania analizy dziennika monitorowania według obiektów</span><span class="sxs-lookup"><span data-stu-id="84d93-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="84d93-113">To polecenie usuwa rozwiązanie analiza dziennika monitorowania według obiektu.</span><span class="sxs-lookup"><span data-stu-id="84d93-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="84d93-114">Przykład 3: usuwanie rozwiązania analizy dzienników według rurociągu</span><span class="sxs-lookup"><span data-stu-id="84d93-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="84d93-115">To polecenie umożliwia usunięcie rozwiązania analizy dziennika monitora według rurociągu.</span><span class="sxs-lookup"><span data-stu-id="84d93-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="84d93-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84d93-116">PARAMETERS</span></span>

### <span data-ttu-id="84d93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d93-117">-DefaultProfile</span></span>
<span data-ttu-id="84d93-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84d93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84d93-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84d93-119">-InputObject</span></span>
<span data-ttu-id="84d93-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="84d93-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="84d93-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84d93-121">-Name</span></span>
<span data-ttu-id="84d93-122">Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="84d93-122">User Solution Name.</span></span>

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

### <span data-ttu-id="84d93-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84d93-123">-PassThru</span></span>
<span data-ttu-id="84d93-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="84d93-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="84d93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d93-125">-ResourceGroupName</span></span>
<span data-ttu-id="84d93-126">Nazwa grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="84d93-126">The name of the resource group to get.</span></span>
<span data-ttu-id="84d93-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="84d93-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="84d93-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="84d93-128">-SubscriptionId</span></span>
<span data-ttu-id="84d93-129">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84d93-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="84d93-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="84d93-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="84d93-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84d93-131">-Confirm</span></span>
<span data-ttu-id="84d93-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d93-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d93-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d93-133">-WhatIf</span></span>
<span data-ttu-id="84d93-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d93-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84d93-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84d93-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d93-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d93-136">CommonParameters</span></span>
<span data-ttu-id="84d93-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d93-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d93-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84d93-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d93-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84d93-139">INPUTS</span></span>

### <span data-ttu-id="84d93-140">Microsoft. Azure. PowerShell. polecenia. MonitoringSolutions. models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="84d93-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="84d93-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84d93-141">OUTPUTS</span></span>

### <span data-ttu-id="84d93-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84d93-142">System.Boolean</span></span>

## <span data-ttu-id="84d93-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84d93-143">NOTES</span></span>

<span data-ttu-id="84d93-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="84d93-144">ALIASES</span></span>

<span data-ttu-id="84d93-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84d93-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="84d93-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="84d93-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84d93-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="84d93-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="84d93-148">INPUTobject <IMonitoringSolutionsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="84d93-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="84d93-149">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="84d93-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="84d93-150">`[ManagementAssociationName <String>]`: Nazwa użytkownika ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="84d93-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="84d93-151">`[ManagementConfigurationName <String>]`: Nazwa konfiguracji zarządzania użytkownikami.</span><span class="sxs-lookup"><span data-stu-id="84d93-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="84d93-152">`[ProviderName <String>]`: Nazwa dostawcy dla zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="84d93-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="84d93-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="84d93-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="84d93-154">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="84d93-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="84d93-155">`[ResourceName <String>]`: Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="84d93-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="84d93-156">`[ResourceType <String>]`: Typ zasobu dla zasobu nadrzędnego</span><span class="sxs-lookup"><span data-stu-id="84d93-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="84d93-157">`[SolutionName <String>]`: Nazwa rozwiązania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="84d93-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="84d93-158">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84d93-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="84d93-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="84d93-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="84d93-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84d93-160">RELATED LINKS</span></span>

