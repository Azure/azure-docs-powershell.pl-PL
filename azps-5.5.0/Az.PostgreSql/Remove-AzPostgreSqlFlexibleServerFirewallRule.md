---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 992312cda46dfa4c038b5c23771c9f7f33bed59b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191410"
---
# <span data-ttu-id="027f1-101">Remove-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="027f1-101">Remove-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="027f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="027f1-102">SYNOPSIS</span></span>
<span data-ttu-id="027f1-103">Usuwa regułę zapory serwera PostgreSQL.</span><span class="sxs-lookup"><span data-stu-id="027f1-103">Deletes a PostgreSQL server firewall rule.</span></span>

## <span data-ttu-id="027f1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="027f1-104">SYNTAX</span></span>

### <span data-ttu-id="027f1-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="027f1-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="027f1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="027f1-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="027f1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="027f1-107">DESCRIPTION</span></span>
<span data-ttu-id="027f1-108">Usuwa regułę zapory serwera PostgreSQL.</span><span class="sxs-lookup"><span data-stu-id="027f1-108">Deletes a PostgreSQL server firewall rule.</span></span>

## <span data-ttu-id="027f1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="027f1-109">EXAMPLES</span></span>

### <span data-ttu-id="027f1-110">Przykład 1. Usuwanie reguły zapory pogresqlowej według nazwy</span><span class="sxs-lookup"><span data-stu-id="027f1-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFlexibleServerFirewallRule -Name firewall-rule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

```

<span data-ttu-id="027f1-111">To polecenie cmdlet usuwa regułę zapory PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="027f1-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="027f1-112">Przykład 2. Usuwanie reguły zapory postgresqlowej za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="027f1-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/firewall-rule-test"
PS C:\> Remove-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID
 
```

<span data-ttu-id="027f1-113">Te polecenia cmdlet usuwają regułę zapory PostgreSql za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="027f1-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="027f1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="027f1-114">PARAMETERS</span></span>

### <span data-ttu-id="027f1-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="027f1-115">-AsJob</span></span>
<span data-ttu-id="027f1-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="027f1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="027f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="027f1-117">-DefaultProfile</span></span>
<span data-ttu-id="027f1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="027f1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="027f1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="027f1-119">-InputObject</span></span>
<span data-ttu-id="027f1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="027f1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="027f1-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="027f1-121">-Name</span></span>
<span data-ttu-id="027f1-122">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="027f1-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="027f1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="027f1-123">-NoWait</span></span>
<span data-ttu-id="027f1-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="027f1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="027f1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="027f1-125">-PassThru</span></span>
<span data-ttu-id="027f1-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="027f1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="027f1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="027f1-127">-ResourceGroupName</span></span>
<span data-ttu-id="027f1-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="027f1-128">The name of the resource group.</span></span>
<span data-ttu-id="027f1-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="027f1-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="027f1-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="027f1-130">-ServerName</span></span>
<span data-ttu-id="027f1-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="027f1-131">The name of the server.</span></span>

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

### <span data-ttu-id="027f1-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="027f1-132">-SubscriptionId</span></span>
<span data-ttu-id="027f1-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="027f1-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="027f1-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="027f1-134">-Confirm</span></span>
<span data-ttu-id="027f1-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="027f1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="027f1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="027f1-136">-WhatIf</span></span>
<span data-ttu-id="027f1-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="027f1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="027f1-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="027f1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="027f1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="027f1-139">CommonParameters</span></span>
<span data-ttu-id="027f1-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="027f1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="027f1-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="027f1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="027f1-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="027f1-142">INPUTS</span></span>

### <span data-ttu-id="027f1-143">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="027f1-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="027f1-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="027f1-144">OUTPUTS</span></span>

### <span data-ttu-id="027f1-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="027f1-145">System.Boolean</span></span>

## <span data-ttu-id="027f1-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="027f1-146">NOTES</span></span>

<span data-ttu-id="027f1-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="027f1-147">ALIASES</span></span>

<span data-ttu-id="027f1-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="027f1-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="027f1-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="027f1-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="027f1-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="027f1-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="027f1-151">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="027f1-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="027f1-152">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="027f1-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="027f1-153">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="027f1-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="027f1-154">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="027f1-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="027f1-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="027f1-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="027f1-156">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="027f1-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="027f1-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="027f1-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="027f1-158">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="027f1-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="027f1-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="027f1-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="027f1-160">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="027f1-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="027f1-161">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="027f1-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="027f1-162">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="027f1-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="027f1-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="027f1-163">RELATED LINKS</span></span>

