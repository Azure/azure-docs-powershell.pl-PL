---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 2867c6f57967da64178e798f3e517715b44d07c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360208"
---
# <span data-ttu-id="f29ae-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="f29ae-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="f29ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f29ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f29ae-103">Tworzenie nowej bazy danych lub aktualizowanie istniejącej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f29ae-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="f29ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f29ae-104">SYNTAX</span></span>

### <span data-ttu-id="f29ae-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f29ae-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f29ae-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f29ae-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f29ae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f29ae-107">DESCRIPTION</span></span>
<span data-ttu-id="f29ae-108">Tworzenie nowej bazy danych lub aktualizowanie istniejącej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f29ae-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="f29ae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f29ae-109">EXAMPLES</span></span>

### <span data-ttu-id="f29ae-110">Przykład 1: aktualizowanie bazy danych serwera MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="f29ae-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="f29ae-111">Zaktualizuj bazę danych według nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="f29ae-111">Update a database by resource name.</span></span>

### <span data-ttu-id="f29ae-112">Przykład 2: aktualizowanie bazy danych MySql według parametru.</span><span class="sxs-lookup"><span data-stu-id="f29ae-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="f29ae-113">Aktualizowanie bazy danych według parametru</span><span class="sxs-lookup"><span data-stu-id="f29ae-113">Update a database by parameter</span></span>

## <span data-ttu-id="f29ae-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f29ae-114">PARAMETERS</span></span>

### <span data-ttu-id="f29ae-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f29ae-115">-AsJob</span></span>
<span data-ttu-id="f29ae-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f29ae-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f29ae-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="f29ae-117">-Charset</span></span>
<span data-ttu-id="f29ae-118">Zestaw znaków dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f29ae-118">The charset of the database.</span></span>

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

### <span data-ttu-id="f29ae-119">— Sortowanie</span><span class="sxs-lookup"><span data-stu-id="f29ae-119">-Collation</span></span>
<span data-ttu-id="f29ae-120">Sortowanie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f29ae-120">The collation of the database.</span></span>

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

### <span data-ttu-id="f29ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29ae-121">-DefaultProfile</span></span>
<span data-ttu-id="f29ae-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f29ae-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f29ae-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f29ae-123">-InputObject</span></span>
<span data-ttu-id="f29ae-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f29ae-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f29ae-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f29ae-125">-Name</span></span>
<span data-ttu-id="f29ae-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f29ae-126">The name of the database.</span></span>

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

### <span data-ttu-id="f29ae-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f29ae-127">-NoWait</span></span>
<span data-ttu-id="f29ae-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f29ae-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f29ae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f29ae-129">-ResourceGroupName</span></span>
<span data-ttu-id="f29ae-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f29ae-130">The name of the resource group.</span></span>
<span data-ttu-id="f29ae-131">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f29ae-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f29ae-132">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f29ae-132">-ServerName</span></span>
<span data-ttu-id="f29ae-133">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f29ae-133">The name of the server.</span></span>

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

### <span data-ttu-id="f29ae-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f29ae-134">-SubscriptionId</span></span>
<span data-ttu-id="f29ae-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f29ae-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f29ae-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f29ae-136">-Confirm</span></span>
<span data-ttu-id="f29ae-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f29ae-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f29ae-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f29ae-138">-WhatIf</span></span>
<span data-ttu-id="f29ae-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f29ae-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f29ae-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f29ae-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f29ae-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29ae-141">CommonParameters</span></span>
<span data-ttu-id="f29ae-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f29ae-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29ae-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f29ae-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29ae-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f29ae-144">INPUTS</span></span>

### <span data-ttu-id="f29ae-145">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f29ae-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f29ae-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f29ae-146">OUTPUTS</span></span>

### <span data-ttu-id="f29ae-147">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="f29ae-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="f29ae-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f29ae-148">NOTES</span></span>

<span data-ttu-id="f29ae-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f29ae-149">ALIASES</span></span>

<span data-ttu-id="f29ae-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f29ae-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f29ae-151">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f29ae-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f29ae-152">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f29ae-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f29ae-153">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f29ae-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f29ae-154">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="f29ae-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f29ae-155">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f29ae-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f29ae-156">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f29ae-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f29ae-157">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f29ae-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f29ae-158">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="f29ae-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="f29ae-159">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f29ae-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f29ae-160">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f29ae-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f29ae-161">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f29ae-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="f29ae-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f29ae-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f29ae-163">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f29ae-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f29ae-164">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f29ae-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f29ae-165">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f29ae-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f29ae-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f29ae-166">RELATED LINKS</span></span>

