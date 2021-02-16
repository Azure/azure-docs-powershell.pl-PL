---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185795"
---
# <span data-ttu-id="0fd23-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="0fd23-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="0fd23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fd23-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd23-103">Usuwa wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="0fd23-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="0fd23-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0fd23-104">SYNTAX</span></span>

### <span data-ttu-id="0fd23-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="0fd23-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0fd23-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0fd23-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0fd23-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0fd23-107">DESCRIPTION</span></span>
<span data-ttu-id="0fd23-108">Usuwa wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="0fd23-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="0fd23-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0fd23-109">EXAMPLES</span></span>

### <span data-ttu-id="0fd23-110">Przykład 1. Usuwanie wystąpienia monitora SAP według nazwy</span><span class="sxs-lookup"><span data-stu-id="0fd23-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="0fd23-111">To polecenie usuwa wystąpienie monitora SAP według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0fd23-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="0fd23-112">Przykład 2. Usuwanie wystąpienia monitora SAP według obiektu</span><span class="sxs-lookup"><span data-stu-id="0fd23-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="0fd23-113">To polecenie usuwa wystąpienie monitora SAP według obiektów.</span><span class="sxs-lookup"><span data-stu-id="0fd23-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="0fd23-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fd23-114">PARAMETERS</span></span>

### <span data-ttu-id="0fd23-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0fd23-115">-AsJob</span></span>
<span data-ttu-id="0fd23-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0fd23-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0fd23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd23-117">-DefaultProfile</span></span>
<span data-ttu-id="0fd23-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd23-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fd23-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fd23-119">-InputObject</span></span>
<span data-ttu-id="0fd23-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0fd23-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd23-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0fd23-121">-Name</span></span>
<span data-ttu-id="0fd23-122">Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="0fd23-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd23-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0fd23-123">-NoWait</span></span>
<span data-ttu-id="0fd23-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0fd23-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0fd23-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fd23-125">-PassThru</span></span>
<span data-ttu-id="0fd23-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="0fd23-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0fd23-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fd23-127">-ResourceGroupName</span></span>
<span data-ttu-id="0fd23-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0fd23-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="0fd23-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="0fd23-129">-SapMonitorName</span></span>
<span data-ttu-id="0fd23-130">Nazwa zasobu monitorowego SAP.</span><span class="sxs-lookup"><span data-stu-id="0fd23-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="0fd23-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0fd23-131">-SubscriptionId</span></span>
<span data-ttu-id="0fd23-132">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd23-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0fd23-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0fd23-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0fd23-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0fd23-134">-Confirm</span></span>
<span data-ttu-id="0fd23-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0fd23-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fd23-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd23-136">-WhatIf</span></span>
<span data-ttu-id="0fd23-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fd23-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fd23-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0fd23-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fd23-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd23-139">CommonParameters</span></span>
<span data-ttu-id="0fd23-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd23-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd23-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fd23-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd23-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fd23-142">INPUTS</span></span>

### <span data-ttu-id="0fd23-143">Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="0fd23-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="0fd23-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fd23-144">OUTPUTS</span></span>

### <span data-ttu-id="0fd23-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0fd23-145">System.Boolean</span></span>

## <span data-ttu-id="0fd23-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0fd23-146">NOTES</span></span>

<span data-ttu-id="0fd23-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0fd23-147">ALIASES</span></span>

<span data-ttu-id="0fd23-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0fd23-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0fd23-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0fd23-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0fd23-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0fd23-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0fd23-151">INPUTOBJECT: <IHanaOnAzureIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="0fd23-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0fd23-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0fd23-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0fd23-153">`[Location <String>]`: lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="0fd23-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="0fd23-154">`[OperationKind <AccessPolicyUpdateKind?>]`: nazwa operacji</span><span class="sxs-lookup"><span data-stu-id="0fd23-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="0fd23-155">`[ProviderInstanceName <String>]`: nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="0fd23-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="0fd23-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0fd23-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="0fd23-157">`[ResourceName <String>]`: nazwa zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="0fd23-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="0fd23-158">`[SapMonitorName <String>]`: nazwa zasobu monitorów SAP.</span><span class="sxs-lookup"><span data-stu-id="0fd23-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="0fd23-159">`[Scope <String>]`: zakres dostawcy zasobów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="0fd23-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="0fd23-160">Zasób nadrzędny jest rozszerzany przez tożsamości zarządzane.</span><span class="sxs-lookup"><span data-stu-id="0fd23-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="0fd23-161">`[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd23-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0fd23-162">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0fd23-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0fd23-163">`[VaultName <String>]`: nazwa magazynu</span><span class="sxs-lookup"><span data-stu-id="0fd23-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="0fd23-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fd23-164">RELATED LINKS</span></span>

