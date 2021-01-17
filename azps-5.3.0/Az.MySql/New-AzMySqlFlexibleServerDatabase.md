---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9d8933aad3b3e24893062e43a3b3232bd0b57cfb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380625"
---
# <span data-ttu-id="4f5ec-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="4f5ec-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="4f5ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5ec-103">Tworzenie nowej bazy danych lub aktualizowanie istniejącej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="4f5ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f5ec-104">SYNTAX</span></span>

### <span data-ttu-id="4f5ec-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4f5ec-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4f5ec-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4f5ec-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4f5ec-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4f5ec-107">DESCRIPTION</span></span>
<span data-ttu-id="4f5ec-108">Tworzenie nowej bazy danych lub aktualizowanie istniejącej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="4f5ec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f5ec-109">EXAMPLES</span></span>

### <span data-ttu-id="4f5ec-110">Przykład 1. Tworzenie nowej bazy danych serwera MySql</span><span class="sxs-lookup"><span data-stu-id="4f5ec-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="4f5ec-111">Utwórz bazę danych z ustawieniami domyślnymi.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-111">Create a database with default settings.</span></span>

## <span data-ttu-id="4f5ec-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f5ec-112">PARAMETERS</span></span>

### <span data-ttu-id="4f5ec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f5ec-113">-AsJob</span></span>
<span data-ttu-id="4f5ec-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4f5ec-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4f5ec-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="4f5ec-115">-Charset</span></span>
<span data-ttu-id="4f5ec-116">Zestaw znaków dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-116">The charset of the database.</span></span>

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

### <span data-ttu-id="4f5ec-117">— Sortowanie</span><span class="sxs-lookup"><span data-stu-id="4f5ec-117">-Collation</span></span>
<span data-ttu-id="4f5ec-118">Sortowanie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-118">The collation of the database.</span></span>

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

### <span data-ttu-id="4f5ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5ec-119">-DefaultProfile</span></span>
<span data-ttu-id="4f5ec-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f5ec-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4f5ec-121">-InputObject</span></span>
<span data-ttu-id="4f5ec-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4f5ec-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4f5ec-123">-Name</span></span>
<span data-ttu-id="4f5ec-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-124">The name of the database.</span></span>

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

### <span data-ttu-id="4f5ec-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4f5ec-125">-NoWait</span></span>
<span data-ttu-id="4f5ec-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4f5ec-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4f5ec-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f5ec-127">-ResourceGroupName</span></span>
<span data-ttu-id="4f5ec-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-128">The name of the resource group.</span></span>
<span data-ttu-id="4f5ec-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4f5ec-130">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4f5ec-130">-ServerName</span></span>
<span data-ttu-id="4f5ec-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-131">The name of the server.</span></span>

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

### <span data-ttu-id="4f5ec-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4f5ec-132">-SubscriptionId</span></span>
<span data-ttu-id="4f5ec-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4f5ec-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4f5ec-134">-Confirm</span></span>
<span data-ttu-id="4f5ec-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f5ec-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f5ec-136">-WhatIf</span></span>
<span data-ttu-id="4f5ec-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f5ec-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f5ec-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5ec-139">CommonParameters</span></span>
<span data-ttu-id="4f5ec-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5ec-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f5ec-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5ec-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f5ec-142">INPUTS</span></span>

### <span data-ttu-id="4f5ec-143">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4f5ec-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4f5ec-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f5ec-144">OUTPUTS</span></span>

### <span data-ttu-id="4f5ec-145">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="4f5ec-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="4f5ec-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f5ec-146">NOTES</span></span>

<span data-ttu-id="4f5ec-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4f5ec-147">ALIASES</span></span>

<span data-ttu-id="4f5ec-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f5ec-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f5ec-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f5ec-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f5ec-151">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4f5ec-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f5ec-152">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4f5ec-153">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4f5ec-154">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4f5ec-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4f5ec-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f5ec-156">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="4f5ec-157">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4f5ec-158">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4f5ec-159">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="4f5ec-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4f5ec-161">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4f5ec-162">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4f5ec-163">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4f5ec-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4f5ec-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f5ec-164">RELATED LINKS</span></span>

