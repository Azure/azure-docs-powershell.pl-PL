---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 979fc45bb7bdfe36133404a88a646a871cb33301
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233858"
---
# <span data-ttu-id="3de94-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3de94-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="3de94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3de94-102">SYNOPSIS</span></span>
<span data-ttu-id="3de94-103">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="3de94-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="3de94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3de94-104">SYNTAX</span></span>

### <span data-ttu-id="3de94-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3de94-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3de94-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3de94-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3de94-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3de94-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3de94-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3de94-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3de94-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3de94-109">DESCRIPTION</span></span>
<span data-ttu-id="3de94-110">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="3de94-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="3de94-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3de94-111">EXAMPLES</span></span>

### <span data-ttu-id="3de94-112">Przykład 1: aktualizowanie reguły zapory MySql na podstawie nazwy</span><span class="sxs-lookup"><span data-stu-id="3de94-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="3de94-113">To polecenie cmdlet powoduje zaktualizowanie reguły zapory MySql na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="3de94-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="3de94-114">Przykład 2: aktualizowanie reguły zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="3de94-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="3de94-115">Te polecenia cmdlet aktualizują regułę zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="3de94-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="3de94-116">Przykład 3: aktualizowanie reguły zapory MySql przed-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="3de94-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="3de94-117">Te polecenia cmdlet aktualizują regułę zapory MySql ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="3de94-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="3de94-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3de94-118">PARAMETERS</span></span>

### <span data-ttu-id="3de94-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3de94-119">-AsJob</span></span>
<span data-ttu-id="3de94-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="3de94-120">Run the command as a job</span></span>

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

### <span data-ttu-id="3de94-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3de94-121">-ClientIPAddress</span></span>
<span data-ttu-id="3de94-122">Klient określił jeden adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="3de94-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="3de94-123">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="3de94-123">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de94-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de94-124">-DefaultProfile</span></span>
<span data-ttu-id="3de94-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3de94-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3de94-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="3de94-126">-EndIPAddress</span></span>
<span data-ttu-id="3de94-127">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="3de94-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="3de94-128">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="3de94-128">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de94-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3de94-129">-InputObject</span></span>
<span data-ttu-id="3de94-130">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3de94-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3de94-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3de94-131">-Name</span></span>
<span data-ttu-id="3de94-132">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="3de94-132">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de94-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3de94-133">-NoWait</span></span>
<span data-ttu-id="3de94-134">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="3de94-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3de94-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de94-135">-ResourceGroupName</span></span>
<span data-ttu-id="3de94-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3de94-136">The name of the resource group.</span></span>
<span data-ttu-id="3de94-137">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="3de94-137">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de94-138">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3de94-138">-ServerName</span></span>
<span data-ttu-id="3de94-139">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="3de94-139">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de94-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="3de94-140">-StartIPAddress</span></span>
<span data-ttu-id="3de94-141">Początkowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="3de94-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="3de94-142">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="3de94-142">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de94-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3de94-143">-SubscriptionId</span></span>
<span data-ttu-id="3de94-144">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3de94-144">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de94-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3de94-145">-Confirm</span></span>
<span data-ttu-id="3de94-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3de94-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3de94-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de94-147">-WhatIf</span></span>
<span data-ttu-id="3de94-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3de94-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de94-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3de94-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3de94-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de94-150">CommonParameters</span></span>
<span data-ttu-id="3de94-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de94-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de94-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3de94-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de94-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3de94-153">INPUTS</span></span>

### <span data-ttu-id="3de94-154">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3de94-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="3de94-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3de94-155">OUTPUTS</span></span>

### <span data-ttu-id="3de94-156">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3de94-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="3de94-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3de94-157">NOTES</span></span>

<span data-ttu-id="3de94-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3de94-158">ALIASES</span></span>

<span data-ttu-id="3de94-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3de94-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3de94-160">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3de94-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3de94-161">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3de94-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3de94-162">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3de94-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3de94-163">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="3de94-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3de94-164">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3de94-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3de94-165">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="3de94-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3de94-166">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3de94-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3de94-167">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="3de94-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3de94-168">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3de94-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3de94-169">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="3de94-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="3de94-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3de94-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3de94-171">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="3de94-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3de94-172">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3de94-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3de94-173">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3de94-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3de94-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3de94-174">RELATED LINKS</span></span>

