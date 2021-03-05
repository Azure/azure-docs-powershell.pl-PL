---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 6f1af89c1557739e218506d441e6acb109fcf773
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979802"
---
# <span data-ttu-id="7945a-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="7945a-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="7945a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7945a-102">SYNOPSIS</span></span>
<span data-ttu-id="7945a-103">Tworzy nową bazę danych lub aktualizuje istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7945a-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="7945a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7945a-104">SYNTAX</span></span>

### <span data-ttu-id="7945a-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="7945a-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7945a-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7945a-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7945a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7945a-107">DESCRIPTION</span></span>
<span data-ttu-id="7945a-108">Tworzy nową bazę danych lub aktualizuje istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7945a-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="7945a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7945a-109">EXAMPLES</span></span>

### <span data-ttu-id="7945a-110">Przykład 1. Tworzenie nowej bazy danych serwera MySql</span><span class="sxs-lookup"><span data-stu-id="7945a-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="7945a-111">Utwórz bazę danych z ustawieniami domyślnymi.</span><span class="sxs-lookup"><span data-stu-id="7945a-111">Create a database with default settings.</span></span>

## <span data-ttu-id="7945a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7945a-112">PARAMETERS</span></span>

### <span data-ttu-id="7945a-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7945a-113">-AsJob</span></span>
<span data-ttu-id="7945a-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="7945a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7945a-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="7945a-115">-Charset</span></span>
<span data-ttu-id="7945a-116">Zestaw znaków bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7945a-116">The charset of the database.</span></span>

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

### <span data-ttu-id="7945a-117">— sortowanie</span><span class="sxs-lookup"><span data-stu-id="7945a-117">-Collation</span></span>
<span data-ttu-id="7945a-118">Sortowanie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7945a-118">The collation of the database.</span></span>

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

### <span data-ttu-id="7945a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7945a-119">-DefaultProfile</span></span>
<span data-ttu-id="7945a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7945a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7945a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7945a-121">-InputObject</span></span>
<span data-ttu-id="7945a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7945a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7945a-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7945a-123">-Name</span></span>
<span data-ttu-id="7945a-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7945a-124">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7945a-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7945a-125">-NoWait</span></span>
<span data-ttu-id="7945a-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="7945a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7945a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7945a-127">-ResourceGroupName</span></span>
<span data-ttu-id="7945a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7945a-128">The name of the resource group.</span></span>
<span data-ttu-id="7945a-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="7945a-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7945a-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7945a-130">-ServerName</span></span>
<span data-ttu-id="7945a-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="7945a-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7945a-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7945a-132">-SubscriptionId</span></span>
<span data-ttu-id="7945a-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7945a-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7945a-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7945a-134">-Confirm</span></span>
<span data-ttu-id="7945a-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7945a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7945a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7945a-136">-WhatIf</span></span>
<span data-ttu-id="7945a-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7945a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7945a-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7945a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7945a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7945a-139">CommonParameters</span></span>
<span data-ttu-id="7945a-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7945a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7945a-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7945a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7945a-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7945a-142">INPUTS</span></span>

### <span data-ttu-id="7945a-143">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7945a-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="7945a-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7945a-144">OUTPUTS</span></span>

### <span data-ttu-id="7945a-145">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iDatabase</span><span class="sxs-lookup"><span data-stu-id="7945a-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="7945a-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7945a-146">NOTES</span></span>

<span data-ttu-id="7945a-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7945a-147">ALIASES</span></span>

<span data-ttu-id="7945a-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7945a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7945a-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7945a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7945a-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7945a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7945a-151">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="7945a-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7945a-152">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="7945a-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7945a-153">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7945a-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7945a-154">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="7945a-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7945a-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7945a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7945a-156">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="7945a-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="7945a-157">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7945a-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7945a-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7945a-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7945a-159">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="7945a-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="7945a-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7945a-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7945a-161">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="7945a-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7945a-162">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7945a-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7945a-163">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7945a-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7945a-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7945a-164">RELATED LINKS</span></span>

