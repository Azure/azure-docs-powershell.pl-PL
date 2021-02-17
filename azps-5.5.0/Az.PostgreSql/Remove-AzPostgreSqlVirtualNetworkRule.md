---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: bacd5e1636457fac172cd54c9fcf4407247d88ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189370"
---
# <span data-ttu-id="8fa58-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8fa58-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="8fa58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fa58-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa58-103">Usuwa regułę sieci wirtualnej z podaną nazwą.</span><span class="sxs-lookup"><span data-stu-id="8fa58-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="8fa58-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8fa58-104">SYNTAX</span></span>

### <span data-ttu-id="8fa58-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="8fa58-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8fa58-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8fa58-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8fa58-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8fa58-107">DESCRIPTION</span></span>
<span data-ttu-id="8fa58-108">Usuwa regułę sieci wirtualnej z podaną nazwą.</span><span class="sxs-lookup"><span data-stu-id="8fa58-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="8fa58-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8fa58-109">EXAMPLES</span></span>

### <span data-ttu-id="8fa58-110">Przykład 1. Usunięcie reguły sieci wirtualnej serwera PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="8fa58-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="8fa58-111">To polecenie cmdlet usuwa regułę wirtualnej sieci serwera PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="8fa58-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="8fa58-112">Przykład 2. Usuwanie reguły sieci wirtualnej serwera PostgreSql przez tożsamość</span><span class="sxs-lookup"><span data-stu-id="8fa58-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="8fa58-113">Te polecenia cmdlet usuwają regułę wirtualnej sieci serwera PostgreSql za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="8fa58-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="8fa58-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fa58-114">PARAMETERS</span></span>

### <span data-ttu-id="8fa58-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8fa58-115">-AsJob</span></span>
<span data-ttu-id="8fa58-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8fa58-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8fa58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa58-117">-DefaultProfile</span></span>
<span data-ttu-id="8fa58-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fa58-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fa58-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fa58-119">-InputObject</span></span>
<span data-ttu-id="8fa58-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8fa58-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8fa58-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8fa58-121">-Name</span></span>
<span data-ttu-id="8fa58-122">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8fa58-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="8fa58-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8fa58-123">-NoWait</span></span>
<span data-ttu-id="8fa58-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8fa58-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8fa58-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fa58-125">-PassThru</span></span>
<span data-ttu-id="8fa58-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="8fa58-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8fa58-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fa58-127">-ResourceGroupName</span></span>
<span data-ttu-id="8fa58-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8fa58-128">The name of the resource group.</span></span>
<span data-ttu-id="8fa58-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="8fa58-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8fa58-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8fa58-130">-ServerName</span></span>
<span data-ttu-id="8fa58-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8fa58-131">The name of the server.</span></span>

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

### <span data-ttu-id="8fa58-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fa58-132">-SubscriptionId</span></span>
<span data-ttu-id="8fa58-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8fa58-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8fa58-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8fa58-134">-Confirm</span></span>
<span data-ttu-id="8fa58-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8fa58-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fa58-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fa58-136">-WhatIf</span></span>
<span data-ttu-id="8fa58-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fa58-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fa58-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8fa58-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fa58-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa58-139">CommonParameters</span></span>
<span data-ttu-id="8fa58-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa58-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa58-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fa58-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa58-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fa58-142">INPUTS</span></span>

### <span data-ttu-id="8fa58-143">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8fa58-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="8fa58-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8fa58-144">OUTPUTS</span></span>

### <span data-ttu-id="8fa58-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8fa58-145">System.Boolean</span></span>

## <span data-ttu-id="8fa58-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8fa58-146">NOTES</span></span>

<span data-ttu-id="8fa58-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8fa58-147">ALIASES</span></span>

<span data-ttu-id="8fa58-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="8fa58-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8fa58-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8fa58-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8fa58-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8fa58-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8fa58-151">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="8fa58-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8fa58-152">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="8fa58-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8fa58-153">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8fa58-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8fa58-154">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8fa58-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8fa58-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8fa58-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8fa58-156">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8fa58-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8fa58-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8fa58-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8fa58-158">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="8fa58-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="8fa58-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="8fa58-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8fa58-160">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8fa58-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8fa58-161">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8fa58-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8fa58-162">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8fa58-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8fa58-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fa58-163">RELATED LINKS</span></span>

