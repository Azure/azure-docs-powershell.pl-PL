---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 656fbdc012f4e6de5f80c88a20cde42a49244618
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241171"
---
# <span data-ttu-id="f15b5-101">Remove-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="f15b5-101">Remove-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="f15b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f15b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f15b5-103">Usuwa bazę danych.</span><span class="sxs-lookup"><span data-stu-id="f15b5-103">Deletes a database.</span></span>

## <span data-ttu-id="f15b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f15b5-104">SYNTAX</span></span>

### <span data-ttu-id="f15b5-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="f15b5-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f15b5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f15b5-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f15b5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f15b5-107">DESCRIPTION</span></span>
<span data-ttu-id="f15b5-108">Usuwa bazę danych.</span><span class="sxs-lookup"><span data-stu-id="f15b5-108">Deletes a database.</span></span>

## <span data-ttu-id="f15b5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f15b5-109">EXAMPLES</span></span>

### <span data-ttu-id="f15b5-110">Przykład 1. Usuwanie bazy danych MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="f15b5-110">Example 1: Remove MySql database by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
```

<span data-ttu-id="f15b5-111">To polecenie cmdlet usuwa bazę danych MySql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f15b5-111">This cmdlet removes MySql database by name.</span></span>

### <span data-ttu-id="f15b5-112">Przykład 2. Usuwanie bazy danych MySql za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="f15b5-112">Example 2: Remove MySql database by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/databases/databasetest"
PS C:\> Remove-AzMySqlFlexibleServerDatabase -InputObject $ID
 
```

<span data-ttu-id="f15b5-113">Te polecenia cmdlet usuwają bazę danych MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f15b5-113">These cmdlets remove MySql database by identity.</span></span>

## <span data-ttu-id="f15b5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f15b5-114">PARAMETERS</span></span>

### <span data-ttu-id="f15b5-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f15b5-115">-AsJob</span></span>
<span data-ttu-id="f15b5-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f15b5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f15b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f15b5-117">-DefaultProfile</span></span>
<span data-ttu-id="f15b5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f15b5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f15b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f15b5-119">-InputObject</span></span>
<span data-ttu-id="f15b5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f15b5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f15b5-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f15b5-121">-Name</span></span>
<span data-ttu-id="f15b5-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f15b5-122">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15b5-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f15b5-123">-NoWait</span></span>
<span data-ttu-id="f15b5-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f15b5-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f15b5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f15b5-125">-PassThru</span></span>
<span data-ttu-id="f15b5-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="f15b5-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f15b5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f15b5-127">-ResourceGroupName</span></span>
<span data-ttu-id="f15b5-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f15b5-128">The name of the resource group.</span></span>
<span data-ttu-id="f15b5-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f15b5-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f15b5-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f15b5-130">-ServerName</span></span>
<span data-ttu-id="f15b5-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f15b5-131">The name of the server.</span></span>

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

### <span data-ttu-id="f15b5-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f15b5-132">-SubscriptionId</span></span>
<span data-ttu-id="f15b5-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f15b5-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f15b5-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f15b5-134">-Confirm</span></span>
<span data-ttu-id="f15b5-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f15b5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f15b5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f15b5-136">-WhatIf</span></span>
<span data-ttu-id="f15b5-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f15b5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f15b5-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f15b5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f15b5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15b5-139">CommonParameters</span></span>
<span data-ttu-id="f15b5-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f15b5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15b5-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f15b5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15b5-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f15b5-142">INPUTS</span></span>

### <span data-ttu-id="f15b5-143">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f15b5-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f15b5-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f15b5-144">OUTPUTS</span></span>

### <span data-ttu-id="f15b5-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f15b5-145">System.Boolean</span></span>

## <span data-ttu-id="f15b5-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f15b5-146">NOTES</span></span>

<span data-ttu-id="f15b5-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f15b5-147">ALIASES</span></span>

<span data-ttu-id="f15b5-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f15b5-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f15b5-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f15b5-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f15b5-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f15b5-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f15b5-151">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="f15b5-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f15b5-152">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="f15b5-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f15b5-153">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f15b5-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f15b5-154">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f15b5-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f15b5-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f15b5-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f15b5-156">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="f15b5-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="f15b5-157">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f15b5-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f15b5-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f15b5-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f15b5-159">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f15b5-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="f15b5-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f15b5-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f15b5-161">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f15b5-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f15b5-162">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f15b5-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f15b5-163">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f15b5-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f15b5-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f15b5-164">RELATED LINKS</span></span>

