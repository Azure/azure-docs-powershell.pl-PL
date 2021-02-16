---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 224d60bdeca8b8884be02a716159374f5d0e31c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192091"
---
# <span data-ttu-id="f8938-101">Remove-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f8938-101">Remove-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="f8938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8938-102">SYNOPSIS</span></span>
<span data-ttu-id="f8938-103">Usuwa regułę sieci wirtualnej z podaną nazwą.</span><span class="sxs-lookup"><span data-stu-id="f8938-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="f8938-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f8938-104">SYNTAX</span></span>

### <span data-ttu-id="f8938-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="f8938-105">Delete (Default)</span></span>
```
Remove-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f8938-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f8938-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8938-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f8938-107">DESCRIPTION</span></span>
<span data-ttu-id="f8938-108">Usuwa regułę sieci wirtualnej z podaną nazwą.</span><span class="sxs-lookup"><span data-stu-id="f8938-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="f8938-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f8938-109">EXAMPLES</span></span>

### <span data-ttu-id="f8938-110">Przykład 1. Usuwanie reguły wirtualnej sieci serwera MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="f8938-110">Example 1: Remove MySql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest-ServerName mysql-test

```

<span data-ttu-id="f8938-111">To polecenie cmdlet usuwa regułę wirtualnej sieci na serwerze MySql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f8938-111">This cmdlet removes MySql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="f8938-112">Przykład 2. Usuwanie reguły sieci wirtualnej serwera MySql za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="f8938-112">Example 2: Remove MySql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Remove-AzMySqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="f8938-113">Te polecenia cmdlet usuwają regułę wirtualnej sieci serwera MySql za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f8938-113">These cmdlets remove MySql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="f8938-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8938-114">PARAMETERS</span></span>

### <span data-ttu-id="f8938-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f8938-115">-AsJob</span></span>
<span data-ttu-id="f8938-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f8938-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f8938-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8938-117">-DefaultProfile</span></span>
<span data-ttu-id="f8938-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8938-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8938-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8938-119">-InputObject</span></span>
<span data-ttu-id="f8938-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f8938-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f8938-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f8938-121">-Name</span></span>
<span data-ttu-id="f8938-122">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f8938-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8938-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f8938-123">-NoWait</span></span>
<span data-ttu-id="f8938-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f8938-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f8938-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8938-125">-PassThru</span></span>
<span data-ttu-id="f8938-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="f8938-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f8938-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8938-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8938-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8938-128">The name of the resource group.</span></span>
<span data-ttu-id="f8938-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f8938-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f8938-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f8938-130">-ServerName</span></span>
<span data-ttu-id="f8938-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f8938-131">The name of the server.</span></span>

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

### <span data-ttu-id="f8938-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8938-132">-SubscriptionId</span></span>
<span data-ttu-id="f8938-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f8938-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f8938-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8938-134">-Confirm</span></span>
<span data-ttu-id="f8938-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f8938-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8938-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8938-136">-WhatIf</span></span>
<span data-ttu-id="f8938-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8938-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8938-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f8938-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8938-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8938-139">CommonParameters</span></span>
<span data-ttu-id="f8938-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8938-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8938-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8938-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8938-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8938-142">INPUTS</span></span>

### <span data-ttu-id="f8938-143">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f8938-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f8938-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8938-144">OUTPUTS</span></span>

### <span data-ttu-id="f8938-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f8938-145">System.Boolean</span></span>

## <span data-ttu-id="f8938-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f8938-146">NOTES</span></span>

<span data-ttu-id="f8938-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f8938-147">ALIASES</span></span>

<span data-ttu-id="f8938-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8938-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8938-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f8938-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8938-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f8938-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8938-151">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="f8938-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8938-152">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="f8938-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f8938-153">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f8938-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f8938-154">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f8938-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f8938-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f8938-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8938-156">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="f8938-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="f8938-157">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f8938-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f8938-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8938-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f8938-159">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f8938-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="f8938-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f8938-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f8938-161">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f8938-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f8938-162">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f8938-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f8938-163">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f8938-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f8938-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8938-164">RELATED LINKS</span></span>

