---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
ms.openlocfilehash: 481761efe01646a10118d8ebfd645375caafbfef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339433"
---
# <span data-ttu-id="9cafc-101">Remove-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9cafc-101">Remove-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="9cafc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cafc-102">SYNOPSIS</span></span>
<span data-ttu-id="9cafc-103">Usuwa regułę zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9cafc-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="9cafc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cafc-104">SYNTAX</span></span>

### <span data-ttu-id="9cafc-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9cafc-105">Delete (Default)</span></span>
```
Remove-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9cafc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9cafc-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9cafc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9cafc-107">DESCRIPTION</span></span>
<span data-ttu-id="9cafc-108">Usuwa regułę zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9cafc-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="9cafc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cafc-109">EXAMPLES</span></span>

### <span data-ttu-id="9cafc-110">Przykład 1: Usuwanie reguły zapory MySql na podstawie nazwy</span><span class="sxs-lookup"><span data-stu-id="9cafc-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="9cafc-111">To polecenie cmdlet powoduje usunięcie reguły zapory MySql na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="9cafc-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="9cafc-112">Przykład 2: Usuwanie reguły zapory MySql przez tożsamość</span><span class="sxs-lookup"><span data-stu-id="9cafc-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Remove-AzMySqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="9cafc-113">Te polecenia cmdlet usuwają regułę zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="9cafc-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="9cafc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cafc-114">PARAMETERS</span></span>

### <span data-ttu-id="9cafc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cafc-115">-AsJob</span></span>
<span data-ttu-id="9cafc-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9cafc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9cafc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cafc-117">-DefaultProfile</span></span>
<span data-ttu-id="9cafc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cafc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cafc-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9cafc-119">-InputObject</span></span>
<span data-ttu-id="9cafc-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9cafc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9cafc-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9cafc-121">-Name</span></span>
<span data-ttu-id="9cafc-122">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9cafc-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="9cafc-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9cafc-123">-NoWait</span></span>
<span data-ttu-id="9cafc-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9cafc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9cafc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cafc-125">-PassThru</span></span>
<span data-ttu-id="9cafc-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="9cafc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9cafc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cafc-127">-ResourceGroupName</span></span>
<span data-ttu-id="9cafc-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9cafc-128">The name of the resource group.</span></span>
<span data-ttu-id="9cafc-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="9cafc-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9cafc-130">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="9cafc-130">-ServerName</span></span>
<span data-ttu-id="9cafc-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9cafc-131">The name of the server.</span></span>

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

### <span data-ttu-id="9cafc-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9cafc-132">-SubscriptionId</span></span>
<span data-ttu-id="9cafc-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9cafc-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9cafc-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cafc-134">-Confirm</span></span>
<span data-ttu-id="9cafc-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cafc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cafc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cafc-136">-WhatIf</span></span>
<span data-ttu-id="9cafc-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cafc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cafc-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9cafc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cafc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cafc-139">CommonParameters</span></span>
<span data-ttu-id="9cafc-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cafc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cafc-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cafc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cafc-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cafc-142">INPUTS</span></span>

### <span data-ttu-id="9cafc-143">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9cafc-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9cafc-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cafc-144">OUTPUTS</span></span>

### <span data-ttu-id="9cafc-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9cafc-145">System.Boolean</span></span>

## <span data-ttu-id="9cafc-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cafc-146">NOTES</span></span>

<span data-ttu-id="9cafc-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9cafc-147">ALIASES</span></span>

<span data-ttu-id="9cafc-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cafc-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9cafc-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9cafc-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9cafc-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9cafc-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9cafc-151">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="9cafc-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9cafc-152">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="9cafc-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9cafc-153">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9cafc-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9cafc-154">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9cafc-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9cafc-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9cafc-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9cafc-156">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="9cafc-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="9cafc-157">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9cafc-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9cafc-158">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9cafc-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9cafc-159">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="9cafc-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="9cafc-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="9cafc-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9cafc-161">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9cafc-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9cafc-162">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9cafc-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9cafc-163">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9cafc-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9cafc-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cafc-164">RELATED LINKS</span></span>

