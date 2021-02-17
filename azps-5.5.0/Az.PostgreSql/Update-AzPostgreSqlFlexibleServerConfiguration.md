---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 82945caa08fb102c0ef5a05e95586f9c66d3d4a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183987"
---
# <span data-ttu-id="72ab9-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="72ab9-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="72ab9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="72ab9-103">Aktualizuje konfigurację serwera.</span><span class="sxs-lookup"><span data-stu-id="72ab9-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="72ab9-104">Użyj Update-AzPostgreSqlFlexibleServer, jeśli chcesz zaktualizować hasło AdministratorLoginPassword, sku itp.</span><span class="sxs-lookup"><span data-stu-id="72ab9-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="72ab9-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="72ab9-105">SYNTAX</span></span>

### <span data-ttu-id="72ab9-106">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="72ab9-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="72ab9-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="72ab9-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="72ab9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="72ab9-108">DESCRIPTION</span></span>
<span data-ttu-id="72ab9-109">Aktualizuje konfigurację serwera.</span><span class="sxs-lookup"><span data-stu-id="72ab9-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="72ab9-110">Użyj Update-AzPostgreSqlFlexibleServer, jeśli chcesz zaktualizować hasło AdministratorLoginPassword, sku itp.</span><span class="sxs-lookup"><span data-stu-id="72ab9-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="72ab9-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="72ab9-111">EXAMPLES</span></span>

### <span data-ttu-id="72ab9-112">Przykład 1. Updatae określonej konfiguracji PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="72ab9-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="72ab9-113">To polecenie cmdlet aktualizuje określoną konfigurację PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="72ab9-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="72ab9-114">Przykład 1. Updatae określonej konfiguracji PostgreSql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="72ab9-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="72ab9-115">To polecenie cmdlet aktualizuje określoną konfigurację PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="72ab9-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="72ab9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72ab9-116">PARAMETERS</span></span>

### <span data-ttu-id="72ab9-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="72ab9-117">-AsJob</span></span>
<span data-ttu-id="72ab9-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="72ab9-118">Run the command as a job</span></span>

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

### <span data-ttu-id="72ab9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ab9-119">-DefaultProfile</span></span>
<span data-ttu-id="72ab9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="72ab9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72ab9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72ab9-121">-InputObject</span></span>
<span data-ttu-id="72ab9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="72ab9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72ab9-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="72ab9-123">-Name</span></span>
<span data-ttu-id="72ab9-124">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="72ab9-124">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab9-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="72ab9-125">-NoWait</span></span>
<span data-ttu-id="72ab9-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="72ab9-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="72ab9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72ab9-127">-ResourceGroupName</span></span>
<span data-ttu-id="72ab9-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72ab9-128">The name of the resource group.</span></span>
<span data-ttu-id="72ab9-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="72ab9-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab9-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72ab9-130">-ServerName</span></span>
<span data-ttu-id="72ab9-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="72ab9-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab9-132">— Źródło</span><span class="sxs-lookup"><span data-stu-id="72ab9-132">-Source</span></span>
<span data-ttu-id="72ab9-133">Źródło konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="72ab9-133">Source of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab9-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72ab9-134">-SubscriptionId</span></span>
<span data-ttu-id="72ab9-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="72ab9-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab9-136">— Wartość</span><span class="sxs-lookup"><span data-stu-id="72ab9-136">-Value</span></span>
<span data-ttu-id="72ab9-137">Wartość konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="72ab9-137">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab9-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72ab9-138">-Confirm</span></span>
<span data-ttu-id="72ab9-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72ab9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ab9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ab9-140">-WhatIf</span></span>
<span data-ttu-id="72ab9-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72ab9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72ab9-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="72ab9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ab9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ab9-143">CommonParameters</span></span>
<span data-ttu-id="72ab9-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ab9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ab9-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72ab9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ab9-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72ab9-146">INPUTS</span></span>

### <span data-ttu-id="72ab9-147">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="72ab9-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="72ab9-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72ab9-148">OUTPUTS</span></span>

### <span data-ttu-id="72ab9-149">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="72ab9-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="72ab9-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="72ab9-150">NOTES</span></span>

<span data-ttu-id="72ab9-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="72ab9-151">ALIASES</span></span>

<span data-ttu-id="72ab9-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72ab9-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="72ab9-153">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="72ab9-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="72ab9-154">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="72ab9-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="72ab9-155">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="72ab9-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="72ab9-156">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="72ab9-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="72ab9-157">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="72ab9-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="72ab9-158">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="72ab9-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="72ab9-159">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="72ab9-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="72ab9-160">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="72ab9-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="72ab9-161">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72ab9-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="72ab9-162">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="72ab9-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="72ab9-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="72ab9-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="72ab9-164">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="72ab9-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="72ab9-165">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="72ab9-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="72ab9-166">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72ab9-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="72ab9-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72ab9-167">RELATED LINKS</span></span>

