---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: c0af624683e3d12cc1b12c057caa419c5633d45f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953530"
---
# <span data-ttu-id="07029-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="07029-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="07029-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07029-102">SYNOPSIS</span></span>
<span data-ttu-id="07029-103">Aktualizuje konfigurację serwera.</span><span class="sxs-lookup"><span data-stu-id="07029-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="07029-104">Użyj Update-AzPostgreSqlServer, jeśli chcesz zaktualizować hasło AdministratorLoginPassword, sku itp.</span><span class="sxs-lookup"><span data-stu-id="07029-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="07029-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="07029-105">SYNTAX</span></span>

### <span data-ttu-id="07029-106">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="07029-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="07029-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="07029-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="07029-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="07029-108">DESCRIPTION</span></span>
<span data-ttu-id="07029-109">Aktualizuje konfigurację serwera.</span><span class="sxs-lookup"><span data-stu-id="07029-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="07029-110">Użyj Update-AzPostgreSqlServer, jeśli chcesz zaktualizować hasło AdministratorLoginPassword, sku itp.</span><span class="sxs-lookup"><span data-stu-id="07029-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="07029-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="07029-111">EXAMPLES</span></span>

### <span data-ttu-id="07029-112">Przykład 1. Aktualizowanie konfiguracji postgresql według nazwy</span><span class="sxs-lookup"><span data-stu-id="07029-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="07029-113">To polecenie cmdlet aktualizuje konfigurację PostgreSql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="07029-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="07029-114">Przykład 2. Aktualizowanie konfiguracji postgresql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="07029-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="07029-115">Te polecenia cmdlet aktualizują konfigurację PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="07029-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="07029-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07029-116">PARAMETERS</span></span>

### <span data-ttu-id="07029-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="07029-117">-AsJob</span></span>
<span data-ttu-id="07029-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="07029-118">Run the command as a job</span></span>

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

### <span data-ttu-id="07029-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07029-119">-DefaultProfile</span></span>
<span data-ttu-id="07029-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="07029-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07029-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07029-121">-InputObject</span></span>
<span data-ttu-id="07029-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="07029-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="07029-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="07029-123">-Name</span></span>
<span data-ttu-id="07029-124">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="07029-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="07029-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="07029-125">-NoWait</span></span>
<span data-ttu-id="07029-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="07029-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="07029-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07029-127">-ResourceGroupName</span></span>
<span data-ttu-id="07029-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="07029-128">The name of the resource group.</span></span>
<span data-ttu-id="07029-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="07029-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="07029-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="07029-130">-ServerName</span></span>
<span data-ttu-id="07029-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="07029-131">The name of the server.</span></span>

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

### <span data-ttu-id="07029-132">— Źródło</span><span class="sxs-lookup"><span data-stu-id="07029-132">-Source</span></span>
<span data-ttu-id="07029-133">Źródło konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="07029-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="07029-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07029-134">-SubscriptionId</span></span>
<span data-ttu-id="07029-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="07029-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="07029-136">— Wartość</span><span class="sxs-lookup"><span data-stu-id="07029-136">-Value</span></span>
<span data-ttu-id="07029-137">Wartość konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="07029-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="07029-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07029-138">-Confirm</span></span>
<span data-ttu-id="07029-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="07029-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07029-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07029-140">-WhatIf</span></span>
<span data-ttu-id="07029-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07029-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07029-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="07029-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07029-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07029-143">CommonParameters</span></span>
<span data-ttu-id="07029-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07029-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07029-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07029-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07029-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07029-146">INPUTS</span></span>

### <span data-ttu-id="07029-147">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="07029-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="07029-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07029-148">OUTPUTS</span></span>

### <span data-ttu-id="07029-149">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="07029-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="07029-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="07029-150">NOTES</span></span>

<span data-ttu-id="07029-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="07029-151">ALIASES</span></span>

<span data-ttu-id="07029-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07029-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07029-153">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="07029-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07029-154">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="07029-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07029-155">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="07029-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="07029-156">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="07029-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="07029-157">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="07029-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="07029-158">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="07029-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="07029-159">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="07029-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="07029-160">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="07029-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="07029-161">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="07029-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="07029-162">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="07029-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="07029-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="07029-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="07029-164">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="07029-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="07029-165">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="07029-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="07029-166">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="07029-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="07029-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07029-167">RELATED LINKS</span></span>

