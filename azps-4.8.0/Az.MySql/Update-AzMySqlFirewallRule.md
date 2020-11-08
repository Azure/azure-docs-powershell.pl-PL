---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 979fc45bb7bdfe36133404a88a646a871cb33301
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063446"
---
# <span data-ttu-id="0de8b-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0de8b-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="0de8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0de8b-102">SYNOPSIS</span></span>
<span data-ttu-id="0de8b-103">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="0de8b-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0de8b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0de8b-104">SYNTAX</span></span>

### <span data-ttu-id="0de8b-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0de8b-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0de8b-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0de8b-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0de8b-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0de8b-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0de8b-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0de8b-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0de8b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="0de8b-109">DESCRIPTION</span></span>
<span data-ttu-id="0de8b-110">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="0de8b-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0de8b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0de8b-111">EXAMPLES</span></span>

### <span data-ttu-id="0de8b-112">Przykład 1: aktualizowanie reguły zapory MySql na podstawie nazwy</span><span class="sxs-lookup"><span data-stu-id="0de8b-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="0de8b-113">To polecenie cmdlet powoduje zaktualizowanie reguły zapory MySql na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="0de8b-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="0de8b-114">Przykład 2: aktualizowanie reguły zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="0de8b-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="0de8b-115">Te polecenia cmdlet aktualizują regułę zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="0de8b-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="0de8b-116">Przykład 3: aktualizowanie reguły zapory MySql przed-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="0de8b-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="0de8b-117">Te polecenia cmdlet aktualizują regułę zapory MySql ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="0de8b-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="0de8b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0de8b-118">PARAMETERS</span></span>

### <span data-ttu-id="0de8b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0de8b-119">-AsJob</span></span>
<span data-ttu-id="0de8b-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0de8b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="0de8b-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0de8b-121">-ClientIPAddress</span></span>
<span data-ttu-id="0de8b-122">Klient określił jeden adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0de8b-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="0de8b-123">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="0de8b-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0de8b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de8b-124">-DefaultProfile</span></span>
<span data-ttu-id="0de8b-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0de8b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0de8b-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="0de8b-126">-EndIPAddress</span></span>
<span data-ttu-id="0de8b-127">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0de8b-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="0de8b-128">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="0de8b-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0de8b-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0de8b-129">-InputObject</span></span>
<span data-ttu-id="0de8b-130">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0de8b-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0de8b-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0de8b-131">-Name</span></span>
<span data-ttu-id="0de8b-132">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0de8b-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="0de8b-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0de8b-133">-NoWait</span></span>
<span data-ttu-id="0de8b-134">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0de8b-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0de8b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de8b-135">-ResourceGroupName</span></span>
<span data-ttu-id="0de8b-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0de8b-136">The name of the resource group.</span></span>
<span data-ttu-id="0de8b-137">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0de8b-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0de8b-138">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0de8b-138">-ServerName</span></span>
<span data-ttu-id="0de8b-139">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0de8b-139">The name of the server.</span></span>

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

### <span data-ttu-id="0de8b-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="0de8b-140">-StartIPAddress</span></span>
<span data-ttu-id="0de8b-141">Początkowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0de8b-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="0de8b-142">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="0de8b-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0de8b-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0de8b-143">-SubscriptionId</span></span>
<span data-ttu-id="0de8b-144">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0de8b-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0de8b-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0de8b-145">-Confirm</span></span>
<span data-ttu-id="0de8b-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de8b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de8b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0de8b-147">-WhatIf</span></span>
<span data-ttu-id="0de8b-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de8b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0de8b-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0de8b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0de8b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de8b-150">CommonParameters</span></span>
<span data-ttu-id="0de8b-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de8b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de8b-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0de8b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de8b-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0de8b-153">INPUTS</span></span>

### <span data-ttu-id="0de8b-154">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0de8b-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0de8b-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0de8b-155">OUTPUTS</span></span>

### <span data-ttu-id="0de8b-156">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0de8b-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="0de8b-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0de8b-157">NOTES</span></span>

<span data-ttu-id="0de8b-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0de8b-158">ALIASES</span></span>

<span data-ttu-id="0de8b-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0de8b-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0de8b-160">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0de8b-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0de8b-161">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0de8b-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0de8b-162">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="0de8b-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0de8b-163">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="0de8b-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0de8b-164">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0de8b-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0de8b-165">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0de8b-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0de8b-166">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0de8b-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0de8b-167">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0de8b-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0de8b-168">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0de8b-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0de8b-169">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0de8b-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="0de8b-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="0de8b-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0de8b-171">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0de8b-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0de8b-172">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0de8b-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0de8b-173">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0de8b-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0de8b-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0de8b-174">RELATED LINKS</span></span>

