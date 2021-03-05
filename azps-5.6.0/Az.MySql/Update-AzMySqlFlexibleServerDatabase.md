---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 7d356bc977ce02d998230ad755f43479e09f0a66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968778"
---
# <span data-ttu-id="ac808-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="ac808-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="ac808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac808-102">SYNOPSIS</span></span>
<span data-ttu-id="ac808-103">Tworzy nową bazę danych lub aktualizuje istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="ac808-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="ac808-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ac808-104">SYNTAX</span></span>

### <span data-ttu-id="ac808-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="ac808-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ac808-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ac808-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac808-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ac808-107">DESCRIPTION</span></span>
<span data-ttu-id="ac808-108">Tworzy nową bazę danych lub aktualizuje istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="ac808-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="ac808-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ac808-109">EXAMPLES</span></span>

### <span data-ttu-id="ac808-110">Przykład 1. Aktualizowanie bazy danych serwera MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="ac808-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="ac808-111">Aktualizowanie bazy danych według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="ac808-111">Update a database by resource name.</span></span>

### <span data-ttu-id="ac808-112">Przykład 2. Aktualizowanie bazy danych MySql według parametru.</span><span class="sxs-lookup"><span data-stu-id="ac808-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="ac808-113">Aktualizowanie bazy danych według parametru</span><span class="sxs-lookup"><span data-stu-id="ac808-113">Update a database by parameter</span></span>

## <span data-ttu-id="ac808-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac808-114">PARAMETERS</span></span>

### <span data-ttu-id="ac808-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ac808-115">-AsJob</span></span>
<span data-ttu-id="ac808-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ac808-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ac808-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="ac808-117">-Charset</span></span>
<span data-ttu-id="ac808-118">Zestaw znaków bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ac808-118">The charset of the database.</span></span>

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

### <span data-ttu-id="ac808-119">— sortowanie</span><span class="sxs-lookup"><span data-stu-id="ac808-119">-Collation</span></span>
<span data-ttu-id="ac808-120">Sortowanie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ac808-120">The collation of the database.</span></span>

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

### <span data-ttu-id="ac808-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac808-121">-DefaultProfile</span></span>
<span data-ttu-id="ac808-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac808-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac808-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac808-123">-InputObject</span></span>
<span data-ttu-id="ac808-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ac808-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac808-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ac808-125">-Name</span></span>
<span data-ttu-id="ac808-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ac808-126">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac808-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ac808-127">-NoWait</span></span>
<span data-ttu-id="ac808-128">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ac808-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac808-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac808-129">-ResourceGroupName</span></span>
<span data-ttu-id="ac808-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ac808-130">The name of the resource group.</span></span>
<span data-ttu-id="ac808-131">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ac808-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ac808-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ac808-132">-ServerName</span></span>
<span data-ttu-id="ac808-133">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ac808-133">The name of the server.</span></span>

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

### <span data-ttu-id="ac808-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac808-134">-SubscriptionId</span></span>
<span data-ttu-id="ac808-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ac808-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ac808-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac808-136">-Confirm</span></span>
<span data-ttu-id="ac808-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ac808-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac808-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac808-138">-WhatIf</span></span>
<span data-ttu-id="ac808-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac808-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac808-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ac808-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac808-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac808-141">CommonParameters</span></span>
<span data-ttu-id="ac808-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac808-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac808-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac808-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac808-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac808-144">INPUTS</span></span>

### <span data-ttu-id="ac808-145">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ac808-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ac808-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac808-146">OUTPUTS</span></span>

### <span data-ttu-id="ac808-147">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iDatabase</span><span class="sxs-lookup"><span data-stu-id="ac808-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="ac808-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ac808-148">NOTES</span></span>

<span data-ttu-id="ac808-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ac808-149">ALIASES</span></span>

<span data-ttu-id="ac808-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac808-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac808-151">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ac808-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac808-152">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac808-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac808-153">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ac808-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac808-154">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="ac808-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ac808-155">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ac808-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ac808-156">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ac808-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ac808-157">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ac808-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac808-158">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="ac808-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ac808-159">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ac808-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ac808-160">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ac808-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ac808-161">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ac808-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="ac808-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ac808-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ac808-163">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ac808-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ac808-164">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ac808-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ac808-165">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ac808-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ac808-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac808-166">RELATED LINKS</span></span>

