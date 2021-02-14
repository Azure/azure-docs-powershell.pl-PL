---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
ms.openlocfilehash: 481761efe01646a10118d8ebfd645375caafbfef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190042"
---
# <span data-ttu-id="2ba63-101">Remove-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2ba63-101">Remove-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="2ba63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ba63-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba63-103">Usuwa regułę zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="2ba63-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="2ba63-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ba63-104">SYNTAX</span></span>

### <span data-ttu-id="2ba63-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="2ba63-105">Delete (Default)</span></span>
```
Remove-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2ba63-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2ba63-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ba63-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ba63-107">DESCRIPTION</span></span>
<span data-ttu-id="2ba63-108">Usuwa regułę zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="2ba63-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="2ba63-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ba63-109">EXAMPLES</span></span>

### <span data-ttu-id="2ba63-110">Przykład 1. Usuwanie reguły zapory MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="2ba63-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="2ba63-111">To polecenie cmdlet usuwa regułę zapory MySql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="2ba63-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="2ba63-112">Przykład 2. Usuwanie reguły zapory MySql za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="2ba63-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Remove-AzMySqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="2ba63-113">Te polecenia cmdlet usuwają regułę zapory MySql za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2ba63-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="2ba63-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ba63-114">PARAMETERS</span></span>

### <span data-ttu-id="2ba63-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2ba63-115">-AsJob</span></span>
<span data-ttu-id="2ba63-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="2ba63-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2ba63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba63-117">-DefaultProfile</span></span>
<span data-ttu-id="2ba63-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ba63-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ba63-119">-InputObject</span></span>
<span data-ttu-id="2ba63-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2ba63-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2ba63-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ba63-121">-Name</span></span>
<span data-ttu-id="2ba63-122">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="2ba63-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="2ba63-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2ba63-123">-NoWait</span></span>
<span data-ttu-id="2ba63-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="2ba63-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2ba63-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ba63-125">-PassThru</span></span>
<span data-ttu-id="2ba63-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="2ba63-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2ba63-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba63-127">-ResourceGroupName</span></span>
<span data-ttu-id="2ba63-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ba63-128">The name of the resource group.</span></span>
<span data-ttu-id="2ba63-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="2ba63-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2ba63-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2ba63-130">-ServerName</span></span>
<span data-ttu-id="2ba63-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="2ba63-131">The name of the server.</span></span>

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

### <span data-ttu-id="2ba63-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ba63-132">-SubscriptionId</span></span>
<span data-ttu-id="2ba63-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2ba63-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2ba63-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ba63-134">-Confirm</span></span>
<span data-ttu-id="2ba63-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ba63-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba63-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba63-136">-WhatIf</span></span>
<span data-ttu-id="2ba63-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba63-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ba63-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2ba63-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ba63-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba63-139">CommonParameters</span></span>
<span data-ttu-id="2ba63-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba63-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba63-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ba63-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba63-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ba63-142">INPUTS</span></span>

### <span data-ttu-id="2ba63-143">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2ba63-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="2ba63-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ba63-144">OUTPUTS</span></span>

### <span data-ttu-id="2ba63-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ba63-145">System.Boolean</span></span>

## <span data-ttu-id="2ba63-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ba63-146">NOTES</span></span>

<span data-ttu-id="2ba63-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2ba63-147">ALIASES</span></span>

<span data-ttu-id="2ba63-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ba63-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ba63-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2ba63-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ba63-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ba63-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ba63-151">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="2ba63-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ba63-152">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="2ba63-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2ba63-153">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2ba63-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2ba63-154">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="2ba63-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2ba63-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2ba63-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ba63-156">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="2ba63-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="2ba63-157">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2ba63-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2ba63-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ba63-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2ba63-159">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="2ba63-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="2ba63-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="2ba63-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2ba63-161">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="2ba63-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2ba63-162">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2ba63-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2ba63-163">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ba63-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2ba63-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ba63-164">RELATED LINKS</span></span>

