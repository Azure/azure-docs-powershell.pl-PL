---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179075"
---
# <span data-ttu-id="edf40-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="edf40-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="edf40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edf40-102">SYNOPSIS</span></span>
<span data-ttu-id="edf40-103">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="edf40-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="edf40-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="edf40-104">SYNTAX</span></span>

### <span data-ttu-id="edf40-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="edf40-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="edf40-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="edf40-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="edf40-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="edf40-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="edf40-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="edf40-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="edf40-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="edf40-109">DESCRIPTION</span></span>
<span data-ttu-id="edf40-110">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="edf40-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="edf40-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="edf40-111">EXAMPLES</span></span>

### <span data-ttu-id="edf40-112">Przykład 1. Aktualizowanie reguły zapory pogresqlowej według nazwy</span><span class="sxs-lookup"><span data-stu-id="edf40-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="edf40-113">To polecenie cmdlet aktualizuje regułę zapory PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="edf40-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="edf40-114">Przykład 2. Aktualizowanie reguły zapory pogresql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="edf40-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="edf40-115">Te polecenia cmdlet aktualizują regułę zapory postgresql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="edf40-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="edf40-116">Przykład 3. Aktualizowanie reguły zapory postgresql przez -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="edf40-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="edf40-117">Te polecenia cmdlet aktualizują regułę zapory PostgreSql przez -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="edf40-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="edf40-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edf40-118">PARAMETERS</span></span>

### <span data-ttu-id="edf40-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="edf40-119">-AsJob</span></span>
<span data-ttu-id="edf40-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="edf40-120">Run the command as a job</span></span>

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

### <span data-ttu-id="edf40-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="edf40-121">-ClientIPAddress</span></span>
<span data-ttu-id="edf40-122">Określony przez klienta pojedynczy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="edf40-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="edf40-123">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="edf40-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="edf40-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf40-124">-DefaultProfile</span></span>
<span data-ttu-id="edf40-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="edf40-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edf40-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="edf40-126">-EndIPAddress</span></span>
<span data-ttu-id="edf40-127">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="edf40-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="edf40-128">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="edf40-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="edf40-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edf40-129">-InputObject</span></span>
<span data-ttu-id="edf40-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="edf40-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edf40-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="edf40-131">-Name</span></span>
<span data-ttu-id="edf40-132">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="edf40-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="edf40-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="edf40-133">-NoWait</span></span>
<span data-ttu-id="edf40-134">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="edf40-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="edf40-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf40-135">-ResourceGroupName</span></span>
<span data-ttu-id="edf40-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="edf40-136">The name of the resource group.</span></span>
<span data-ttu-id="edf40-137">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="edf40-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="edf40-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="edf40-138">-ServerName</span></span>
<span data-ttu-id="edf40-139">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="edf40-139">The name of the server.</span></span>

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

### <span data-ttu-id="edf40-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="edf40-140">-StartIPAddress</span></span>
<span data-ttu-id="edf40-141">Adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="edf40-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="edf40-142">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="edf40-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="edf40-143">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="edf40-143">-SubscriptionId</span></span>
<span data-ttu-id="edf40-144">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="edf40-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="edf40-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edf40-145">-Confirm</span></span>
<span data-ttu-id="edf40-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="edf40-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edf40-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edf40-147">-WhatIf</span></span>
<span data-ttu-id="edf40-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edf40-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edf40-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="edf40-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edf40-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf40-150">CommonParameters</span></span>
<span data-ttu-id="edf40-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf40-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf40-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edf40-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf40-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edf40-153">INPUTS</span></span>

### <span data-ttu-id="edf40-154">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="edf40-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="edf40-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edf40-155">OUTPUTS</span></span>

### <span data-ttu-id="edf40-156">Microsoft.Azure.PowerShell.cmdlet.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="edf40-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="edf40-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="edf40-157">NOTES</span></span>

<span data-ttu-id="edf40-158">ALIASY</span><span class="sxs-lookup"><span data-stu-id="edf40-158">ALIASES</span></span>

<span data-ttu-id="edf40-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edf40-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="edf40-160">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="edf40-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="edf40-161">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="edf40-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="edf40-162">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="edf40-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="edf40-163">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="edf40-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="edf40-164">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="edf40-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="edf40-165">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="edf40-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="edf40-166">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="edf40-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="edf40-167">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="edf40-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="edf40-168">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="edf40-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="edf40-169">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="edf40-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="edf40-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="edf40-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="edf40-171">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="edf40-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="edf40-172">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="edf40-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="edf40-173">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="edf40-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="edf40-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edf40-174">RELATED LINKS</span></span>

