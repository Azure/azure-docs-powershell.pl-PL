---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7775c4adeef0ce4b05efa2b54c6484408256f3eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203675"
---
# <span data-ttu-id="19403-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="19403-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="19403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19403-102">SYNOPSIS</span></span>
<span data-ttu-id="19403-103">Usuwa regułę zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="19403-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="19403-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="19403-104">SYNTAX</span></span>

### <span data-ttu-id="19403-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="19403-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="19403-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19403-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="19403-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="19403-107">DESCRIPTION</span></span>
<span data-ttu-id="19403-108">Usuwa regułę zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="19403-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="19403-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="19403-109">EXAMPLES</span></span>

### <span data-ttu-id="19403-110">Przykład 1. Usunięcie reguły zapory z bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="19403-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="19403-111">To polecenie usuwa regułę zapory w bazie danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="19403-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="19403-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19403-112">PARAMETERS</span></span>

### <span data-ttu-id="19403-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="19403-113">-AsJob</span></span>
<span data-ttu-id="19403-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="19403-114">Run the command as a job</span></span>

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

### <span data-ttu-id="19403-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19403-115">-DefaultProfile</span></span>
<span data-ttu-id="19403-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="19403-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19403-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19403-117">-InputObject</span></span>
<span data-ttu-id="19403-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="19403-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19403-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="19403-119">-Name</span></span>
<span data-ttu-id="19403-120">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="19403-120">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19403-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="19403-121">-NoWait</span></span>
<span data-ttu-id="19403-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="19403-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="19403-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19403-123">-PassThru</span></span>
<span data-ttu-id="19403-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="19403-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="19403-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19403-125">-ResourceGroupName</span></span>
<span data-ttu-id="19403-126">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="19403-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="19403-127">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="19403-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="19403-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="19403-128">-ServerName</span></span>
<span data-ttu-id="19403-129">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="19403-129">The name of the server.</span></span>

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

### <span data-ttu-id="19403-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19403-130">-SubscriptionId</span></span>
<span data-ttu-id="19403-131">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19403-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="19403-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19403-132">-Confirm</span></span>
<span data-ttu-id="19403-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="19403-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19403-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19403-134">-WhatIf</span></span>
<span data-ttu-id="19403-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19403-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19403-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="19403-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19403-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19403-137">CommonParameters</span></span>
<span data-ttu-id="19403-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19403-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19403-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19403-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19403-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19403-140">INPUTS</span></span>

### <span data-ttu-id="19403-141">Microsoft.Azure.PowerShell.Cmdlet.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="19403-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="19403-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19403-142">OUTPUTS</span></span>

### <span data-ttu-id="19403-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19403-143">System.Boolean</span></span>

## <span data-ttu-id="19403-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="19403-144">NOTES</span></span>

<span data-ttu-id="19403-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="19403-145">ALIASES</span></span>

<span data-ttu-id="19403-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="19403-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19403-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="19403-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19403-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="19403-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19403-149">INPUTOBJECT: <IMariaDbIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="19403-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19403-150">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="19403-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="19403-151">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="19403-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="19403-152">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="19403-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="19403-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="19403-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19403-154">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="19403-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="19403-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="19403-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="19403-156">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="19403-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="19403-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="19403-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="19403-158">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="19403-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="19403-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19403-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="19403-160">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19403-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="19403-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19403-161">RELATED LINKS</span></span>

