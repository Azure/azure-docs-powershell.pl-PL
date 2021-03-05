---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 850b1cfae70abb3e1225f9ff7bcda937dc0f0db4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003882"
---
# <span data-ttu-id="b9ff1-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b9ff1-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="b9ff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ff1-103">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b9ff1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b9ff1-104">SYNTAX</span></span>

### <span data-ttu-id="b9ff1-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="b9ff1-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b9ff1-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b9ff1-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b9ff1-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b9ff1-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b9ff1-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b9ff1-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9ff1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b9ff1-109">DESCRIPTION</span></span>
<span data-ttu-id="b9ff1-110">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b9ff1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b9ff1-111">EXAMPLES</span></span>

### <span data-ttu-id="b9ff1-112">Przykład 1. Aktualizowanie reguły zapory MariaDB</span><span class="sxs-lookup"><span data-stu-id="b9ff1-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="b9ff1-113">To polecenie aktualizuje regułę zapory mariadb.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="b9ff1-114">Przykład 2. Aktualizowanie reguły zapory MariaDB przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b9ff1-115">Polecenie cmdlet aktualizuje regułę zapory MariaDB za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="b9ff1-116">Przykład 3. Aktualizowanie reguły zapory MariaDB przez -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="b9ff1-117">Polecenie cmdlet aktualizuje regułę zapory MariaDB przez -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="b9ff1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9ff1-118">PARAMETERS</span></span>

### <span data-ttu-id="b9ff1-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b9ff1-119">-AsJob</span></span>
<span data-ttu-id="b9ff1-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b9ff1-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b9ff1-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b9ff1-121">-ClientIPAddress</span></span>
<span data-ttu-id="b9ff1-122">Określony przez klienta pojedynczy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b9ff1-123">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-123">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ff1-124">-DefaultProfile</span></span>
<span data-ttu-id="b9ff1-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9ff1-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b9ff1-126">-EndIPAddress</span></span>
<span data-ttu-id="b9ff1-127">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b9ff1-128">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-128">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9ff1-129">-InputObject</span></span>
<span data-ttu-id="b9ff1-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b9ff1-131">-Name</span></span>
<span data-ttu-id="b9ff1-132">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-132">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b9ff1-133">-NoWait</span></span>
<span data-ttu-id="b9ff1-134">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b9ff1-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b9ff1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ff1-135">-ResourceGroupName</span></span>
<span data-ttu-id="b9ff1-136">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b9ff1-137">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9ff1-138">-ServerName</span></span>
<span data-ttu-id="b9ff1-139">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-139">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b9ff1-140">-StartIPAddress</span></span>
<span data-ttu-id="b9ff1-141">Adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b9ff1-142">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-142">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-143">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9ff1-143">-SubscriptionId</span></span>
<span data-ttu-id="b9ff1-144">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-144">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9ff1-145">-Confirm</span></span>
<span data-ttu-id="b9ff1-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9ff1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ff1-147">-WhatIf</span></span>
<span data-ttu-id="b9ff1-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9ff1-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9ff1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ff1-150">CommonParameters</span></span>
<span data-ttu-id="b9ff1-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ff1-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9ff1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ff1-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9ff1-153">INPUTS</span></span>

### <span data-ttu-id="b9ff1-154">Microsoft.Azure.PowerShell.Cmdlet.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="b9ff1-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="b9ff1-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9ff1-155">OUTPUTS</span></span>

### <span data-ttu-id="b9ff1-156">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b9ff1-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="b9ff1-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b9ff1-157">NOTES</span></span>

<span data-ttu-id="b9ff1-158">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b9ff1-158">ALIASES</span></span>

<span data-ttu-id="b9ff1-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9ff1-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9ff1-160">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9ff1-161">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9ff1-162">INPUTOBJECT: <IMariaDbIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b9ff1-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9ff1-163">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b9ff1-164">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b9ff1-165">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b9ff1-166">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b9ff1-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9ff1-167">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b9ff1-168">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b9ff1-169">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b9ff1-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b9ff1-171">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b9ff1-172">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="b9ff1-173">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b9ff1-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9ff1-174">RELATED LINKS</span></span>

