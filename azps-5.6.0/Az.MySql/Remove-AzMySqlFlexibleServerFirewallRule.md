---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/remove-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 651b2cdc1a7e9c6002d87a78c77a6a48cc561af7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006529"
---
# <span data-ttu-id="9ee42-101">Remove-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9ee42-101">Remove-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="9ee42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee42-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee42-103">Usuwa regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="9ee42-103">Deletes a firewall rule.</span></span>

## <span data-ttu-id="9ee42-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9ee42-104">SYNTAX</span></span>

### <span data-ttu-id="9ee42-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="9ee42-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9ee42-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9ee42-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9ee42-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9ee42-107">DESCRIPTION</span></span>
<span data-ttu-id="9ee42-108">Usuwa regułę zapory.</span><span class="sxs-lookup"><span data-stu-id="9ee42-108">Deletes a firewall rule.</span></span>

## <span data-ttu-id="9ee42-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9ee42-109">EXAMPLES</span></span>

### <span data-ttu-id="9ee42-110">Przykład 1. Usuwanie reguły zapory MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="9ee42-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServerFirewallRule -Name firewall-rule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="9ee42-111">To polecenie cmdlet usuwa regułę zapory MySql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="9ee42-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="9ee42-112">Przykład 2. Usuwanie reguły zapory MySql za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="9ee42-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/firewall-rule-test"
PS C:\> Remove-AzMySqlFlexibleServerFirewallRule -InputObject $ID
 
```

<span data-ttu-id="9ee42-113">Te polecenia cmdlet usuwają regułę zapory MySql za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9ee42-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="9ee42-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ee42-114">PARAMETERS</span></span>

### <span data-ttu-id="9ee42-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9ee42-115">-AsJob</span></span>
<span data-ttu-id="9ee42-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9ee42-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9ee42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee42-117">-DefaultProfile</span></span>
<span data-ttu-id="9ee42-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ee42-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ee42-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ee42-119">-InputObject</span></span>
<span data-ttu-id="9ee42-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9ee42-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee42-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9ee42-121">-Name</span></span>
<span data-ttu-id="9ee42-122">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9ee42-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="9ee42-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9ee42-123">-NoWait</span></span>
<span data-ttu-id="9ee42-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9ee42-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9ee42-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ee42-125">-PassThru</span></span>
<span data-ttu-id="9ee42-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9ee42-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9ee42-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee42-127">-ResourceGroupName</span></span>
<span data-ttu-id="9ee42-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ee42-128">The name of the resource group.</span></span>
<span data-ttu-id="9ee42-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9ee42-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9ee42-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9ee42-130">-ServerName</span></span>
<span data-ttu-id="9ee42-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9ee42-131">The name of the server.</span></span>

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

### <span data-ttu-id="9ee42-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ee42-132">-SubscriptionId</span></span>
<span data-ttu-id="9ee42-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9ee42-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9ee42-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ee42-134">-Confirm</span></span>
<span data-ttu-id="9ee42-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9ee42-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ee42-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ee42-136">-WhatIf</span></span>
<span data-ttu-id="9ee42-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ee42-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ee42-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9ee42-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ee42-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee42-139">CommonParameters</span></span>
<span data-ttu-id="9ee42-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee42-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee42-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ee42-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee42-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ee42-142">INPUTS</span></span>

### <span data-ttu-id="9ee42-143">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9ee42-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9ee42-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ee42-144">OUTPUTS</span></span>

### <span data-ttu-id="9ee42-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ee42-145">System.Boolean</span></span>

## <span data-ttu-id="9ee42-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9ee42-146">NOTES</span></span>

<span data-ttu-id="9ee42-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9ee42-147">ALIASES</span></span>

<span data-ttu-id="9ee42-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ee42-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9ee42-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9ee42-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9ee42-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9ee42-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9ee42-151">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="9ee42-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9ee42-152">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="9ee42-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9ee42-153">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9ee42-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9ee42-154">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9ee42-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9ee42-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9ee42-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9ee42-156">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="9ee42-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="9ee42-157">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9ee42-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9ee42-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ee42-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9ee42-159">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9ee42-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="9ee42-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="9ee42-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9ee42-161">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9ee42-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9ee42-162">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9ee42-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9ee42-163">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9ee42-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9ee42-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ee42-164">RELATED LINKS</span></span>

