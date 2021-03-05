---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 98e476b2a1732d2c984d200265d817c3ff6d71a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968785"
---
# <span data-ttu-id="4e8b7-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e8b7-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="4e8b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8b7-103">Aktualizuje informacje o konfiguracji serwera elastycznego MySQL.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="4e8b7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4e8b7-104">SYNTAX</span></span>

### <span data-ttu-id="4e8b7-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="4e8b7-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e8b7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4e8b7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e8b7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4e8b7-107">DESCRIPTION</span></span>
<span data-ttu-id="4e8b7-108">Aktualizuje informacje o konfiguracji serwera elastycznego MySQL.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="4e8b7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4e8b7-109">EXAMPLES</span></span>

### <span data-ttu-id="4e8b7-110">Przykład 1. Aktualizowanie konfiguracji mysql według nazwy</span><span class="sxs-lookup"><span data-stu-id="4e8b7-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="4e8b7-111">To polecenie cmdlet aktualizuje konfigurację mysql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="4e8b7-112">Przykład 2. Aktualizowanie konfiguracji mysql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="4e8b7-113">Te polecenia cmdlet aktualizują konfigurację mysql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="4e8b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e8b7-114">PARAMETERS</span></span>

### <span data-ttu-id="4e8b7-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4e8b7-115">-AsJob</span></span>
<span data-ttu-id="4e8b7-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4e8b7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4e8b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8b7-117">-DefaultProfile</span></span>
<span data-ttu-id="4e8b7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e8b7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e8b7-119">-InputObject</span></span>
<span data-ttu-id="4e8b7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e8b7-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4e8b7-121">-Name</span></span>
<span data-ttu-id="4e8b7-122">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="4e8b7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4e8b7-123">-NoWait</span></span>
<span data-ttu-id="4e8b7-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4e8b7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4e8b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e8b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e8b7-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-126">The name of the resource group.</span></span>
<span data-ttu-id="4e8b7-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4e8b7-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e8b7-128">-ServerName</span></span>
<span data-ttu-id="4e8b7-129">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-129">The name of the server.</span></span>

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

### <span data-ttu-id="4e8b7-130">— Źródło</span><span class="sxs-lookup"><span data-stu-id="4e8b7-130">-Source</span></span>
<span data-ttu-id="4e8b7-131">Źródło aktualizowanej wartości.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-131">The source of the updating value.</span></span>
<span data-ttu-id="4e8b7-132">Wartość domyślna to zastępowanie przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="4e8b7-132">The default value is user-override</span></span>

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

### <span data-ttu-id="4e8b7-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e8b7-133">-SubscriptionId</span></span>
<span data-ttu-id="4e8b7-134">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4e8b7-135">— Wartość</span><span class="sxs-lookup"><span data-stu-id="4e8b7-135">-Value</span></span>
<span data-ttu-id="4e8b7-136">Wartość konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="4e8b7-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e8b7-137">-Confirm</span></span>
<span data-ttu-id="4e8b7-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e8b7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e8b7-139">-WhatIf</span></span>
<span data-ttu-id="4e8b7-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e8b7-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e8b7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8b7-142">CommonParameters</span></span>
<span data-ttu-id="4e8b7-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8b7-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e8b7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8b7-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e8b7-145">INPUTS</span></span>

### <span data-ttu-id="4e8b7-146">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4e8b7-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4e8b7-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e8b7-147">OUTPUTS</span></span>

### <span data-ttu-id="4e8b7-148">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="4e8b7-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="4e8b7-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4e8b7-149">NOTES</span></span>

<span data-ttu-id="4e8b7-150">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4e8b7-150">ALIASES</span></span>

<span data-ttu-id="4e8b7-151">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e8b7-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e8b7-152">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e8b7-153">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e8b7-154">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="4e8b7-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e8b7-155">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4e8b7-156">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4e8b7-157">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4e8b7-158">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4e8b7-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e8b7-159">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="4e8b7-160">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4e8b7-161">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4e8b7-162">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="4e8b7-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4e8b7-164">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4e8b7-165">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4e8b7-166">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4e8b7-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4e8b7-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e8b7-167">RELATED LINKS</span></span>

