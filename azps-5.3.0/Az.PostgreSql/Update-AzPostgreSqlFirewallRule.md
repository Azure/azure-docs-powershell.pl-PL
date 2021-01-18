---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501195"
---
# <span data-ttu-id="dbea8-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dbea8-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="dbea8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dbea8-102">SYNOPSIS</span></span>
<span data-ttu-id="dbea8-103">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="dbea8-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="dbea8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dbea8-104">SYNTAX</span></span>

### <span data-ttu-id="dbea8-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dbea8-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dbea8-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="dbea8-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dbea8-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dbea8-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dbea8-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dbea8-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dbea8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="dbea8-109">DESCRIPTION</span></span>
<span data-ttu-id="dbea8-110">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="dbea8-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="dbea8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dbea8-111">EXAMPLES</span></span>

### <span data-ttu-id="dbea8-112">Przykład 1: aktualizowanie reguły zapory PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="dbea8-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="dbea8-113">To polecenie cmdlet aktualizuje PostgreSqlą regułę zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="dbea8-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="dbea8-114">Przykład 2: aktualizowanie reguły zapory PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="dbea8-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="dbea8-115">Te polecenia cmdlet aktualizują regułę zapory PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="dbea8-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="dbea8-116">Przykład 3: aktualizowanie reguły zapory PostgreSql przez-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="dbea8-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="dbea8-117">Te polecenia cmdlet aktualizują regułę zapory PostgreSql przez-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="dbea8-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="dbea8-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbea8-118">PARAMETERS</span></span>

### <span data-ttu-id="dbea8-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbea8-119">-AsJob</span></span>
<span data-ttu-id="dbea8-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="dbea8-120">Run the command as a job</span></span>

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

### <span data-ttu-id="dbea8-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="dbea8-121">-ClientIPAddress</span></span>
<span data-ttu-id="dbea8-122">Klient określił jeden adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="dbea8-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="dbea8-123">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="dbea8-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="dbea8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbea8-124">-DefaultProfile</span></span>
<span data-ttu-id="dbea8-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbea8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbea8-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="dbea8-126">-EndIPAddress</span></span>
<span data-ttu-id="dbea8-127">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="dbea8-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="dbea8-128">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="dbea8-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="dbea8-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dbea8-129">-InputObject</span></span>
<span data-ttu-id="dbea8-130">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="dbea8-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dbea8-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dbea8-131">-Name</span></span>
<span data-ttu-id="dbea8-132">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="dbea8-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="dbea8-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="dbea8-133">-NoWait</span></span>
<span data-ttu-id="dbea8-134">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="dbea8-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dbea8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbea8-135">-ResourceGroupName</span></span>
<span data-ttu-id="dbea8-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dbea8-136">The name of the resource group.</span></span>
<span data-ttu-id="dbea8-137">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="dbea8-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dbea8-138">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="dbea8-138">-ServerName</span></span>
<span data-ttu-id="dbea8-139">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="dbea8-139">The name of the server.</span></span>

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

### <span data-ttu-id="dbea8-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="dbea8-140">-StartIPAddress</span></span>
<span data-ttu-id="dbea8-141">Początkowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="dbea8-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="dbea8-142">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="dbea8-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="dbea8-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dbea8-143">-SubscriptionId</span></span>
<span data-ttu-id="dbea8-144">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="dbea8-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dbea8-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dbea8-145">-Confirm</span></span>
<span data-ttu-id="dbea8-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbea8-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbea8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbea8-147">-WhatIf</span></span>
<span data-ttu-id="dbea8-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbea8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbea8-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dbea8-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbea8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbea8-150">CommonParameters</span></span>
<span data-ttu-id="dbea8-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbea8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbea8-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbea8-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbea8-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbea8-153">INPUTS</span></span>

### <span data-ttu-id="dbea8-154">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="dbea8-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="dbea8-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dbea8-155">OUTPUTS</span></span>

### <span data-ttu-id="dbea8-156">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dbea8-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="dbea8-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dbea8-157">NOTES</span></span>

<span data-ttu-id="dbea8-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="dbea8-158">ALIASES</span></span>

<span data-ttu-id="dbea8-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbea8-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dbea8-160">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="dbea8-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dbea8-161">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dbea8-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dbea8-162">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="dbea8-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dbea8-163">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="dbea8-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dbea8-164">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="dbea8-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dbea8-165">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="dbea8-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dbea8-166">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="dbea8-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dbea8-167">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dbea8-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dbea8-168">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dbea8-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dbea8-169">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="dbea8-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="dbea8-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="dbea8-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dbea8-171">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="dbea8-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dbea8-172">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="dbea8-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dbea8-173">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dbea8-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dbea8-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbea8-174">RELATED LINKS</span></span>

