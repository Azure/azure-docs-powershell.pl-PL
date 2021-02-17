---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: fe6ef1a5193119c4778d18c39a7ecff98354cf89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240314"
---
# <span data-ttu-id="9435b-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9435b-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="9435b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9435b-102">SYNOPSIS</span></span>
<span data-ttu-id="9435b-103">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="9435b-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="9435b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9435b-104">SYNTAX</span></span>

### <span data-ttu-id="9435b-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="9435b-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9435b-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9435b-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9435b-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9435b-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9435b-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9435b-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9435b-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="9435b-109">DESCRIPTION</span></span>
<span data-ttu-id="9435b-110">Tworzy nową regułę zapory lub aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="9435b-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="9435b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9435b-111">EXAMPLES</span></span>

### <span data-ttu-id="9435b-112">Przykład 1. Aktualizowanie reguły zapory pogresqlowej według nazwy</span><span class="sxs-lookup"><span data-stu-id="9435b-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="9435b-113">To polecenie cmdlet aktualizuje regułę zapory PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="9435b-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="9435b-114">Przykład 2. Aktualizowanie reguły zapory pogresql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="9435b-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="9435b-115">Te polecenia cmdlet aktualizują regułę zapory postgresql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9435b-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="9435b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9435b-116">PARAMETERS</span></span>

### <span data-ttu-id="9435b-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9435b-117">-AsJob</span></span>
<span data-ttu-id="9435b-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9435b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="9435b-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9435b-119">-ClientIPAddress</span></span>
<span data-ttu-id="9435b-120">Określony przez klienta pojedynczy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9435b-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="9435b-121">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="9435b-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9435b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9435b-122">-DefaultProfile</span></span>
<span data-ttu-id="9435b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9435b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9435b-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="9435b-124">-EndIPAddress</span></span>
<span data-ttu-id="9435b-125">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9435b-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="9435b-126">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="9435b-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9435b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9435b-127">-InputObject</span></span>
<span data-ttu-id="9435b-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9435b-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9435b-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9435b-129">-Name</span></span>
<span data-ttu-id="9435b-130">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9435b-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="9435b-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9435b-131">-NoWait</span></span>
<span data-ttu-id="9435b-132">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9435b-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9435b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9435b-133">-ResourceGroupName</span></span>
<span data-ttu-id="9435b-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9435b-134">The name of the resource group.</span></span>
<span data-ttu-id="9435b-135">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9435b-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9435b-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9435b-136">-ServerName</span></span>
<span data-ttu-id="9435b-137">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9435b-137">The name of the server.</span></span>

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

### <span data-ttu-id="9435b-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="9435b-138">-StartIPAddress</span></span>
<span data-ttu-id="9435b-139">Adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9435b-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="9435b-140">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="9435b-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9435b-141">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9435b-141">-SubscriptionId</span></span>
<span data-ttu-id="9435b-142">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9435b-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9435b-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9435b-143">-Confirm</span></span>
<span data-ttu-id="9435b-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9435b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9435b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9435b-145">-WhatIf</span></span>
<span data-ttu-id="9435b-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9435b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9435b-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9435b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9435b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9435b-148">CommonParameters</span></span>
<span data-ttu-id="9435b-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9435b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9435b-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9435b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9435b-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9435b-151">INPUTS</span></span>

### <span data-ttu-id="9435b-152">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9435b-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="9435b-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9435b-153">OUTPUTS</span></span>

### <span data-ttu-id="9435b-154">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9435b-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="9435b-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9435b-155">NOTES</span></span>

<span data-ttu-id="9435b-156">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9435b-156">ALIASES</span></span>

<span data-ttu-id="9435b-157">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9435b-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9435b-158">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9435b-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9435b-159">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9435b-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9435b-160">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="9435b-160">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9435b-161">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="9435b-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9435b-162">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9435b-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9435b-163">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9435b-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9435b-164">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9435b-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9435b-165">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9435b-165">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9435b-166">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9435b-166">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9435b-167">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9435b-167">The name is case insensitive.</span></span>
  - <span data-ttu-id="9435b-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="9435b-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9435b-169">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9435b-169">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9435b-170">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9435b-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9435b-171">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9435b-171">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9435b-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9435b-172">RELATED LINKS</span></span>

