---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: e45d342f7bb02034b2adf0473e6d4d1eb3c2b370
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974657"
---
# <span data-ttu-id="fe462-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe462-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="fe462-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe462-102">SYNOPSIS</span></span>
<span data-ttu-id="fe462-103">Aktualizuje konfigurację serwera.</span><span class="sxs-lookup"><span data-stu-id="fe462-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="fe462-104">Użyj Update-AzPostgreSqlFlexibleServer, jeśli chcesz zaktualizować hasło AdministratorLoginPassword, sku itp.</span><span class="sxs-lookup"><span data-stu-id="fe462-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="fe462-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe462-105">SYNTAX</span></span>

### <span data-ttu-id="fe462-106">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="fe462-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fe462-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fe462-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fe462-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe462-108">DESCRIPTION</span></span>
<span data-ttu-id="fe462-109">Aktualizuje konfigurację serwera.</span><span class="sxs-lookup"><span data-stu-id="fe462-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="fe462-110">Użyj Update-AzPostgreSqlFlexibleServer, jeśli chcesz zaktualizować hasło AdministratorLoginPassword, sku itp.</span><span class="sxs-lookup"><span data-stu-id="fe462-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="fe462-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe462-111">EXAMPLES</span></span>

### <span data-ttu-id="fe462-112">Przykład 1. Updatae określonej konfiguracji PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="fe462-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="fe462-113">To polecenie cmdlet aktualizuje określoną konfigurację PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="fe462-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="fe462-114">Przykład 1. Updatae określonej konfiguracji PostgreSql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="fe462-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="fe462-115">To polecenie cmdlet aktualizuje określoną konfigurację PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="fe462-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="fe462-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe462-116">PARAMETERS</span></span>

### <span data-ttu-id="fe462-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fe462-117">-AsJob</span></span>
<span data-ttu-id="fe462-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="fe462-118">Run the command as a job</span></span>

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

### <span data-ttu-id="fe462-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe462-119">-DefaultProfile</span></span>
<span data-ttu-id="fe462-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe462-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe462-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe462-121">-InputObject</span></span>
<span data-ttu-id="fe462-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fe462-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fe462-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe462-123">-Name</span></span>
<span data-ttu-id="fe462-124">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="fe462-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="fe462-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fe462-125">-NoWait</span></span>
<span data-ttu-id="fe462-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="fe462-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fe462-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe462-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe462-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe462-128">The name of the resource group.</span></span>
<span data-ttu-id="fe462-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="fe462-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fe462-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fe462-130">-ServerName</span></span>
<span data-ttu-id="fe462-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="fe462-131">The name of the server.</span></span>

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

### <span data-ttu-id="fe462-132">— Źródło</span><span class="sxs-lookup"><span data-stu-id="fe462-132">-Source</span></span>
<span data-ttu-id="fe462-133">Źródło konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="fe462-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="fe462-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe462-134">-SubscriptionId</span></span>
<span data-ttu-id="fe462-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="fe462-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fe462-136">— Wartość</span><span class="sxs-lookup"><span data-stu-id="fe462-136">-Value</span></span>
<span data-ttu-id="fe462-137">Wartość konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="fe462-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="fe462-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe462-138">-Confirm</span></span>
<span data-ttu-id="fe462-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fe462-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe462-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe462-140">-WhatIf</span></span>
<span data-ttu-id="fe462-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe462-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe462-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fe462-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe462-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe462-143">CommonParameters</span></span>
<span data-ttu-id="fe462-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe462-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe462-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe462-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe462-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe462-146">INPUTS</span></span>

### <span data-ttu-id="fe462-147">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fe462-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="fe462-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe462-148">OUTPUTS</span></span>

### <span data-ttu-id="fe462-149">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="fe462-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="fe462-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe462-150">NOTES</span></span>

<span data-ttu-id="fe462-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fe462-151">ALIASES</span></span>

<span data-ttu-id="fe462-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe462-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fe462-153">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fe462-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fe462-154">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fe462-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fe462-155">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="fe462-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fe462-156">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="fe462-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fe462-157">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fe462-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fe462-158">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="fe462-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fe462-159">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="fe462-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fe462-160">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="fe462-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fe462-161">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe462-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fe462-162">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="fe462-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="fe462-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="fe462-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fe462-164">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="fe462-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fe462-165">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="fe462-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fe462-166">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fe462-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fe462-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe462-167">RELATED LINKS</span></span>

