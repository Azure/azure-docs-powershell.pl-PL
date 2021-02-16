---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: 6c7576023e4902caacd204edc97feba0a378f63b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192082"
---
# <span data-ttu-id="09f5d-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="09f5d-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="09f5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="09f5d-103">Aktualizuje konfigurację serwera.</span><span class="sxs-lookup"><span data-stu-id="09f5d-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="09f5d-104">Użyj Update-AzMySqlServer, jeśli chcesz zaktualizować hasło AdministratorLoginPassword, sku itp.</span><span class="sxs-lookup"><span data-stu-id="09f5d-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="09f5d-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09f5d-105">SYNTAX</span></span>

### <span data-ttu-id="09f5d-106">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="09f5d-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09f5d-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="09f5d-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09f5d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="09f5d-108">DESCRIPTION</span></span>
<span data-ttu-id="09f5d-109">Aktualizuje konfigurację serwera.</span><span class="sxs-lookup"><span data-stu-id="09f5d-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="09f5d-110">Użyj Update-AzMySqlServer, jeśli chcesz zaktualizować hasło AdministratorLoginPassword, sku itp.</span><span class="sxs-lookup"><span data-stu-id="09f5d-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="09f5d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09f5d-111">EXAMPLES</span></span>

### <span data-ttu-id="09f5d-112">Przykład 1. Aktualizowanie konfiguracji mysql według nazwy</span><span class="sxs-lookup"><span data-stu-id="09f5d-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="09f5d-113">To polecenie cmdlet aktualizuje konfigurację programu MySql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="09f5d-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="09f5d-114">Przykład 2. Aktualizowanie konfiguracji mysql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="09f5d-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="09f5d-115">Te polecenia cmdlet aktualizują konfigurację mysql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="09f5d-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="09f5d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09f5d-116">PARAMETERS</span></span>

### <span data-ttu-id="09f5d-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="09f5d-117">-AsJob</span></span>
<span data-ttu-id="09f5d-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="09f5d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="09f5d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f5d-119">-DefaultProfile</span></span>
<span data-ttu-id="09f5d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="09f5d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09f5d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09f5d-121">-InputObject</span></span>
<span data-ttu-id="09f5d-122">Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="09f5d-122">Identity Parameter.</span></span>
<span data-ttu-id="09f5d-123">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="09f5d-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="09f5d-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="09f5d-124">-Name</span></span>
<span data-ttu-id="09f5d-125">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="09f5d-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="09f5d-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="09f5d-126">-NoWait</span></span>
<span data-ttu-id="09f5d-127">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="09f5d-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="09f5d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f5d-128">-ResourceGroupName</span></span>
<span data-ttu-id="09f5d-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09f5d-129">The name of the resource group.</span></span>
<span data-ttu-id="09f5d-130">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="09f5d-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="09f5d-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="09f5d-131">-ServerName</span></span>
<span data-ttu-id="09f5d-132">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="09f5d-132">The name of the server.</span></span>

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

### <span data-ttu-id="09f5d-133">— Źródło</span><span class="sxs-lookup"><span data-stu-id="09f5d-133">-Source</span></span>
<span data-ttu-id="09f5d-134">Źródło konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="09f5d-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="09f5d-135">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09f5d-135">-SubscriptionId</span></span>
<span data-ttu-id="09f5d-136">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="09f5d-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="09f5d-137">— Wartość</span><span class="sxs-lookup"><span data-stu-id="09f5d-137">-Value</span></span>
<span data-ttu-id="09f5d-138">Wartość konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="09f5d-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="09f5d-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09f5d-139">-Confirm</span></span>
<span data-ttu-id="09f5d-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09f5d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09f5d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09f5d-141">-WhatIf</span></span>
<span data-ttu-id="09f5d-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09f5d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09f5d-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="09f5d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09f5d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f5d-144">CommonParameters</span></span>
<span data-ttu-id="09f5d-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f5d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f5d-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09f5d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f5d-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09f5d-147">INPUTS</span></span>

### <span data-ttu-id="09f5d-148">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="09f5d-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="09f5d-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="09f5d-149">OUTPUTS</span></span>

### <span data-ttu-id="09f5d-150">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="09f5d-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="09f5d-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09f5d-151">NOTES</span></span>

<span data-ttu-id="09f5d-152">ALIASY</span><span class="sxs-lookup"><span data-stu-id="09f5d-152">ALIASES</span></span>

<span data-ttu-id="09f5d-153">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="09f5d-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09f5d-154">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="09f5d-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09f5d-155">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09f5d-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09f5d-156">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="09f5d-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="09f5d-157">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="09f5d-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="09f5d-158">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="09f5d-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="09f5d-159">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="09f5d-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="09f5d-160">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="09f5d-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09f5d-161">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="09f5d-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="09f5d-162">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="09f5d-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="09f5d-163">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09f5d-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="09f5d-164">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="09f5d-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="09f5d-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="09f5d-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="09f5d-166">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="09f5d-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="09f5d-167">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="09f5d-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="09f5d-168">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="09f5d-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="09f5d-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09f5d-169">RELATED LINKS</span></span>

