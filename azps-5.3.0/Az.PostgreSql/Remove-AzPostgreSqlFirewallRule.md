---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 27f03ba80a01997d61bc50f6a644b4e3c4cffb7b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378385"
---
# <span data-ttu-id="8acae-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8acae-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="8acae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8acae-102">SYNOPSIS</span></span>
<span data-ttu-id="8acae-103">Usuwa regułę zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8acae-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="8acae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8acae-104">SYNTAX</span></span>

### <span data-ttu-id="8acae-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8acae-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8acae-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8acae-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8acae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8acae-107">DESCRIPTION</span></span>
<span data-ttu-id="8acae-108">Usuwa regułę zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8acae-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="8acae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8acae-109">EXAMPLES</span></span>

### <span data-ttu-id="8acae-110">Przykład 1: Usuwanie reguły zapory PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="8acae-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="8acae-111">To polecenie cmdlet usuwa PostgreSqlą regułę zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="8acae-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="8acae-112">Przykład 2: Usuwanie reguły zapory PostgreSql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="8acae-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="8acae-113">Te polecenia cmdlet usuwają regułę zapory PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="8acae-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="8acae-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8acae-114">PARAMETERS</span></span>

### <span data-ttu-id="8acae-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8acae-115">-AsJob</span></span>
<span data-ttu-id="8acae-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8acae-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8acae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8acae-117">-DefaultProfile</span></span>
<span data-ttu-id="8acae-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8acae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8acae-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8acae-119">-InputObject</span></span>
<span data-ttu-id="8acae-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8acae-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8acae-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8acae-121">-Name</span></span>
<span data-ttu-id="8acae-122">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8acae-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8acae-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8acae-123">-NoWait</span></span>
<span data-ttu-id="8acae-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8acae-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8acae-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8acae-125">-PassThru</span></span>
<span data-ttu-id="8acae-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="8acae-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8acae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8acae-127">-ResourceGroupName</span></span>
<span data-ttu-id="8acae-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8acae-128">The name of the resource group.</span></span>
<span data-ttu-id="8acae-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8acae-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8acae-130">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8acae-130">-ServerName</span></span>
<span data-ttu-id="8acae-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8acae-131">The name of the server.</span></span>

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

### <span data-ttu-id="8acae-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8acae-132">-SubscriptionId</span></span>
<span data-ttu-id="8acae-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8acae-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8acae-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8acae-134">-Confirm</span></span>
<span data-ttu-id="8acae-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8acae-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8acae-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8acae-136">-WhatIf</span></span>
<span data-ttu-id="8acae-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8acae-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8acae-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8acae-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8acae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8acae-139">CommonParameters</span></span>
<span data-ttu-id="8acae-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8acae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8acae-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8acae-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8acae-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8acae-142">INPUTS</span></span>

### <span data-ttu-id="8acae-143">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8acae-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="8acae-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8acae-144">OUTPUTS</span></span>

### <span data-ttu-id="8acae-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8acae-145">System.Boolean</span></span>

## <span data-ttu-id="8acae-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8acae-146">NOTES</span></span>

<span data-ttu-id="8acae-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8acae-147">ALIASES</span></span>

<span data-ttu-id="8acae-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8acae-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8acae-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8acae-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8acae-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8acae-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8acae-151">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="8acae-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8acae-152">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="8acae-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8acae-153">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8acae-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8acae-154">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8acae-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8acae-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8acae-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8acae-156">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8acae-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8acae-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8acae-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8acae-158">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8acae-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="8acae-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="8acae-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8acae-160">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8acae-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8acae-161">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8acae-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8acae-162">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8acae-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8acae-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8acae-163">RELATED LINKS</span></span>

