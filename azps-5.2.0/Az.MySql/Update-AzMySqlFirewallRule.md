---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: eb74b9530c9ce196b308a310d5a20642328719e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360250"
---
# <span data-ttu-id="b22d3-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b22d3-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="b22d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b22d3-102">SYNOPSIS</span></span>
<span data-ttu-id="b22d3-103">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="b22d3-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b22d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b22d3-104">SYNTAX</span></span>

### <span data-ttu-id="b22d3-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b22d3-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b22d3-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b22d3-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b22d3-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b22d3-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b22d3-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b22d3-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b22d3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b22d3-109">DESCRIPTION</span></span>
<span data-ttu-id="b22d3-110">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="b22d3-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b22d3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b22d3-111">EXAMPLES</span></span>

### <span data-ttu-id="b22d3-112">Przykład 1: aktualizowanie reguły zapory MySql na podstawie nazwy</span><span class="sxs-lookup"><span data-stu-id="b22d3-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b22d3-113">To polecenie cmdlet powoduje zaktualizowanie reguły zapory MySql na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="b22d3-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="b22d3-114">Przykład 2: aktualizowanie reguły zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="b22d3-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b22d3-115">Te polecenia cmdlet aktualizują regułę zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="b22d3-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="b22d3-116">Przykład 3: aktualizowanie reguły zapory MySql przed-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="b22d3-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="b22d3-117">Te polecenia cmdlet aktualizują regułę zapory MySql ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="b22d3-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="b22d3-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b22d3-118">PARAMETERS</span></span>

### <span data-ttu-id="b22d3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b22d3-119">-AsJob</span></span>
<span data-ttu-id="b22d3-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b22d3-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b22d3-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b22d3-121">-ClientIPAddress</span></span>
<span data-ttu-id="b22d3-122">Klient określił jeden adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b22d3-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b22d3-123">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="b22d3-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b22d3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22d3-124">-DefaultProfile</span></span>
<span data-ttu-id="b22d3-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b22d3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b22d3-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b22d3-126">-EndIPAddress</span></span>
<span data-ttu-id="b22d3-127">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b22d3-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b22d3-128">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="b22d3-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b22d3-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b22d3-129">-InputObject</span></span>
<span data-ttu-id="b22d3-130">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b22d3-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b22d3-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b22d3-131">-Name</span></span>
<span data-ttu-id="b22d3-132">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b22d3-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b22d3-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b22d3-133">-NoWait</span></span>
<span data-ttu-id="b22d3-134">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b22d3-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b22d3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22d3-135">-ResourceGroupName</span></span>
<span data-ttu-id="b22d3-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b22d3-136">The name of the resource group.</span></span>
<span data-ttu-id="b22d3-137">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="b22d3-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b22d3-138">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b22d3-138">-ServerName</span></span>
<span data-ttu-id="b22d3-139">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b22d3-139">The name of the server.</span></span>

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

### <span data-ttu-id="b22d3-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b22d3-140">-StartIPAddress</span></span>
<span data-ttu-id="b22d3-141">Początkowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b22d3-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b22d3-142">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="b22d3-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b22d3-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b22d3-143">-SubscriptionId</span></span>
<span data-ttu-id="b22d3-144">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b22d3-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b22d3-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b22d3-145">-Confirm</span></span>
<span data-ttu-id="b22d3-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b22d3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b22d3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22d3-147">-WhatIf</span></span>
<span data-ttu-id="b22d3-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b22d3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b22d3-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b22d3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b22d3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22d3-150">CommonParameters</span></span>
<span data-ttu-id="b22d3-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b22d3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22d3-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b22d3-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22d3-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b22d3-153">INPUTS</span></span>

### <span data-ttu-id="b22d3-154">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b22d3-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b22d3-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b22d3-155">OUTPUTS</span></span>

### <span data-ttu-id="b22d3-156">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b22d3-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="b22d3-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b22d3-157">NOTES</span></span>

<span data-ttu-id="b22d3-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b22d3-158">ALIASES</span></span>

<span data-ttu-id="b22d3-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b22d3-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b22d3-160">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b22d3-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b22d3-161">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b22d3-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b22d3-162">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b22d3-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b22d3-163">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="b22d3-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b22d3-164">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b22d3-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b22d3-165">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b22d3-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b22d3-166">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b22d3-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b22d3-167">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="b22d3-167">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b22d3-168">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b22d3-168">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b22d3-169">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b22d3-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b22d3-170">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="b22d3-170">The name is case insensitive.</span></span>
  - <span data-ttu-id="b22d3-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="b22d3-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b22d3-172">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b22d3-172">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b22d3-173">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b22d3-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b22d3-174">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b22d3-174">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b22d3-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b22d3-175">RELATED LINKS</span></span>

