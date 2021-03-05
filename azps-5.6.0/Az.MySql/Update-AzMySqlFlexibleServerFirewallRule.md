---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 2147921826c6f50882345bc68603b0dae8cb26ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968762"
---
# <span data-ttu-id="4652f-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4652f-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="4652f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4652f-102">SYNOPSIS</span></span>
<span data-ttu-id="4652f-103">Aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="4652f-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="4652f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4652f-104">SYNTAX</span></span>

### <span data-ttu-id="4652f-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="4652f-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4652f-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="4652f-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4652f-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4652f-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4652f-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4652f-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4652f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="4652f-109">DESCRIPTION</span></span>
<span data-ttu-id="4652f-110">Aktualizuje istniejącą regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="4652f-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="4652f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4652f-111">EXAMPLES</span></span>

### <span data-ttu-id="4652f-112">Przykład 1. Aktualizowanie reguły zapory MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="4652f-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="4652f-113">To polecenie cmdlet aktualizuje regułę zapory mysql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="4652f-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="4652f-114">Przykład 2. Aktualizowanie reguły zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="4652f-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="4652f-115">Te polecenia cmdlet aktualizują regułę zapory MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="4652f-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="4652f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4652f-116">PARAMETERS</span></span>

### <span data-ttu-id="4652f-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4652f-117">-AsJob</span></span>
<span data-ttu-id="4652f-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4652f-118">Run the command as a job</span></span>

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

### <span data-ttu-id="4652f-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="4652f-119">-ClientIPAddress</span></span>
<span data-ttu-id="4652f-120">Określony przez klienta pojedynczy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="4652f-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="4652f-121">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="4652f-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4652f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4652f-122">-DefaultProfile</span></span>
<span data-ttu-id="4652f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4652f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4652f-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="4652f-124">-EndIPAddress</span></span>
<span data-ttu-id="4652f-125">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="4652f-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="4652f-126">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="4652f-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4652f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4652f-127">-InputObject</span></span>
<span data-ttu-id="4652f-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4652f-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4652f-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4652f-129">-Name</span></span>
<span data-ttu-id="4652f-130">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="4652f-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="4652f-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4652f-131">-NoWait</span></span>
<span data-ttu-id="4652f-132">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4652f-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4652f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4652f-133">-ResourceGroupName</span></span>
<span data-ttu-id="4652f-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4652f-134">The name of the resource group.</span></span>
<span data-ttu-id="4652f-135">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4652f-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4652f-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4652f-136">-ServerName</span></span>
<span data-ttu-id="4652f-137">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="4652f-137">The name of the server.</span></span>

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

### <span data-ttu-id="4652f-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="4652f-138">-StartIPAddress</span></span>
<span data-ttu-id="4652f-139">Adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="4652f-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="4652f-140">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="4652f-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4652f-141">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4652f-141">-SubscriptionId</span></span>
<span data-ttu-id="4652f-142">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4652f-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4652f-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4652f-143">-Confirm</span></span>
<span data-ttu-id="4652f-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4652f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4652f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4652f-145">-WhatIf</span></span>
<span data-ttu-id="4652f-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4652f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4652f-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4652f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4652f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4652f-148">CommonParameters</span></span>
<span data-ttu-id="4652f-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4652f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4652f-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4652f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4652f-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4652f-151">INPUTS</span></span>

### <span data-ttu-id="4652f-152">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4652f-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4652f-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4652f-153">OUTPUTS</span></span>

### <span data-ttu-id="4652f-154">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4652f-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="4652f-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4652f-155">NOTES</span></span>

<span data-ttu-id="4652f-156">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4652f-156">ALIASES</span></span>

<span data-ttu-id="4652f-157">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4652f-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4652f-158">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4652f-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4652f-159">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4652f-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4652f-160">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="4652f-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4652f-161">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="4652f-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4652f-162">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4652f-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4652f-163">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="4652f-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4652f-164">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4652f-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4652f-165">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="4652f-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="4652f-166">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4652f-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4652f-167">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4652f-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4652f-168">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4652f-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="4652f-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="4652f-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4652f-170">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="4652f-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4652f-171">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4652f-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4652f-172">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4652f-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4652f-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4652f-173">RELATED LINKS</span></span>

