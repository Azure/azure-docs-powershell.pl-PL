---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 5df722564e899d46a1f68bf8e88ecdaa2b792121
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187323"
---
# <span data-ttu-id="72296-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="72296-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="72296-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72296-102">SYNOPSIS</span></span>
<span data-ttu-id="72296-103">Aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="72296-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="72296-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="72296-104">SYNTAX</span></span>

### <span data-ttu-id="72296-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="72296-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="72296-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="72296-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="72296-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="72296-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="72296-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="72296-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="72296-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="72296-109">DESCRIPTION</span></span>
<span data-ttu-id="72296-110">Aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="72296-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="72296-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="72296-111">EXAMPLES</span></span>

### <span data-ttu-id="72296-112">Przykład 1. Aktualizowanie reguły zapory MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="72296-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="72296-113">To polecenie cmdlet aktualizuje regułę zapory mysql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="72296-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="72296-114">Przykład 2. Aktualizowanie reguły zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="72296-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="72296-115">Te polecenia cmdlet aktualizują regułę zapory MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="72296-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="72296-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72296-116">PARAMETERS</span></span>

### <span data-ttu-id="72296-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="72296-117">-AsJob</span></span>
<span data-ttu-id="72296-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="72296-118">Run the command as a job</span></span>

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

### <span data-ttu-id="72296-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="72296-119">-ClientIPAddress</span></span>
<span data-ttu-id="72296-120">Określony przez klienta pojedynczy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="72296-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="72296-121">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="72296-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="72296-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72296-122">-DefaultProfile</span></span>
<span data-ttu-id="72296-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="72296-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72296-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="72296-124">-EndIPAddress</span></span>
<span data-ttu-id="72296-125">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="72296-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="72296-126">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="72296-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="72296-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72296-127">-InputObject</span></span>
<span data-ttu-id="72296-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="72296-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72296-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="72296-129">-Name</span></span>
<span data-ttu-id="72296-130">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="72296-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="72296-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="72296-131">-NoWait</span></span>
<span data-ttu-id="72296-132">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="72296-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="72296-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72296-133">-ResourceGroupName</span></span>
<span data-ttu-id="72296-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72296-134">The name of the resource group.</span></span>
<span data-ttu-id="72296-135">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="72296-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="72296-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72296-136">-ServerName</span></span>
<span data-ttu-id="72296-137">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="72296-137">The name of the server.</span></span>

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

### <span data-ttu-id="72296-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="72296-138">-StartIPAddress</span></span>
<span data-ttu-id="72296-139">Adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="72296-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="72296-140">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="72296-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="72296-141">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72296-141">-SubscriptionId</span></span>
<span data-ttu-id="72296-142">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="72296-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="72296-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72296-143">-Confirm</span></span>
<span data-ttu-id="72296-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72296-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72296-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72296-145">-WhatIf</span></span>
<span data-ttu-id="72296-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72296-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72296-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="72296-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72296-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72296-148">CommonParameters</span></span>
<span data-ttu-id="72296-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72296-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72296-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72296-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72296-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72296-151">INPUTS</span></span>

### <span data-ttu-id="72296-152">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="72296-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="72296-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72296-153">OUTPUTS</span></span>

### <span data-ttu-id="72296-154">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="72296-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="72296-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="72296-155">NOTES</span></span>

<span data-ttu-id="72296-156">ALIASY</span><span class="sxs-lookup"><span data-stu-id="72296-156">ALIASES</span></span>

<span data-ttu-id="72296-157">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72296-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="72296-158">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="72296-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="72296-159">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="72296-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="72296-160">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="72296-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="72296-161">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="72296-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="72296-162">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="72296-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="72296-163">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="72296-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="72296-164">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="72296-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="72296-165">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="72296-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="72296-166">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="72296-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="72296-167">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72296-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="72296-168">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="72296-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="72296-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="72296-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="72296-170">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="72296-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="72296-171">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="72296-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="72296-172">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72296-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="72296-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72296-173">RELATED LINKS</span></span>

