---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331138"
---
# <span data-ttu-id="bd59c-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bd59c-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="bd59c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd59c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd59c-103">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="bd59c-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="bd59c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd59c-104">SYNTAX</span></span>

### <span data-ttu-id="bd59c-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bd59c-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bd59c-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="bd59c-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bd59c-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bd59c-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bd59c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bd59c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bd59c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="bd59c-109">DESCRIPTION</span></span>
<span data-ttu-id="bd59c-110">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="bd59c-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="bd59c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd59c-111">EXAMPLES</span></span>

### <span data-ttu-id="bd59c-112">Przykład 1: aktualizowanie reguły zapory PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="bd59c-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="bd59c-113">To polecenie cmdlet aktualizuje PostgreSqlą regułę zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="bd59c-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="bd59c-114">Przykład 2: aktualizowanie reguły zapory PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bd59c-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="bd59c-115">Te polecenia cmdlet aktualizują regułę zapory PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bd59c-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="bd59c-116">Przykład 3: aktualizowanie reguły zapory PostgreSql przez-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="bd59c-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="bd59c-117">Te polecenia cmdlet aktualizują regułę zapory PostgreSql przez-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="bd59c-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="bd59c-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd59c-118">PARAMETERS</span></span>

### <span data-ttu-id="bd59c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd59c-119">-AsJob</span></span>
<span data-ttu-id="bd59c-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="bd59c-120">Run the command as a job</span></span>

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

### <span data-ttu-id="bd59c-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="bd59c-121">-ClientIPAddress</span></span>
<span data-ttu-id="bd59c-122">Klient określił jeden adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="bd59c-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="bd59c-123">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="bd59c-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="bd59c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd59c-124">-DefaultProfile</span></span>
<span data-ttu-id="bd59c-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd59c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd59c-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="bd59c-126">-EndIPAddress</span></span>
<span data-ttu-id="bd59c-127">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="bd59c-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="bd59c-128">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="bd59c-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="bd59c-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bd59c-129">-InputObject</span></span>
<span data-ttu-id="bd59c-130">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="bd59c-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bd59c-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd59c-131">-Name</span></span>
<span data-ttu-id="bd59c-132">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="bd59c-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="bd59c-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bd59c-133">-NoWait</span></span>
<span data-ttu-id="bd59c-134">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="bd59c-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bd59c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd59c-135">-ResourceGroupName</span></span>
<span data-ttu-id="bd59c-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd59c-136">The name of the resource group.</span></span>
<span data-ttu-id="bd59c-137">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="bd59c-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bd59c-138">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="bd59c-138">-ServerName</span></span>
<span data-ttu-id="bd59c-139">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bd59c-139">The name of the server.</span></span>

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

### <span data-ttu-id="bd59c-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="bd59c-140">-StartIPAddress</span></span>
<span data-ttu-id="bd59c-141">Początkowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="bd59c-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="bd59c-142">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="bd59c-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="bd59c-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bd59c-143">-SubscriptionId</span></span>
<span data-ttu-id="bd59c-144">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="bd59c-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bd59c-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd59c-145">-Confirm</span></span>
<span data-ttu-id="bd59c-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd59c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd59c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd59c-147">-WhatIf</span></span>
<span data-ttu-id="bd59c-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd59c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd59c-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd59c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd59c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd59c-150">CommonParameters</span></span>
<span data-ttu-id="bd59c-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd59c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd59c-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd59c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd59c-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd59c-153">INPUTS</span></span>

### <span data-ttu-id="bd59c-154">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bd59c-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="bd59c-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd59c-155">OUTPUTS</span></span>

### <span data-ttu-id="bd59c-156">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bd59c-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="bd59c-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd59c-157">NOTES</span></span>

<span data-ttu-id="bd59c-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="bd59c-158">ALIASES</span></span>

<span data-ttu-id="bd59c-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd59c-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd59c-160">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bd59c-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd59c-161">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bd59c-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd59c-162">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="bd59c-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bd59c-163">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="bd59c-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bd59c-164">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bd59c-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bd59c-165">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="bd59c-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bd59c-166">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bd59c-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bd59c-167">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="bd59c-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bd59c-168">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd59c-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bd59c-169">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="bd59c-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="bd59c-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="bd59c-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bd59c-171">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bd59c-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bd59c-172">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="bd59c-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bd59c-173">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bd59c-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bd59c-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd59c-174">RELATED LINKS</span></span>

