---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 5df722564e899d46a1f68bf8e88ecdaa2b792121
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360199"
---
# <span data-ttu-id="8d396-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8d396-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="8d396-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d396-102">SYNOPSIS</span></span>
<span data-ttu-id="8d396-103">Umożliwia zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="8d396-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="8d396-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d396-104">SYNTAX</span></span>

### <span data-ttu-id="8d396-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8d396-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d396-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="8d396-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d396-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d396-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d396-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8d396-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8d396-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8d396-109">DESCRIPTION</span></span>
<span data-ttu-id="8d396-110">Umożliwia zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="8d396-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="8d396-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d396-111">EXAMPLES</span></span>

### <span data-ttu-id="8d396-112">Przykład 1: aktualizowanie reguły zapory MySql na podstawie nazwy</span><span class="sxs-lookup"><span data-stu-id="8d396-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="8d396-113">To polecenie cmdlet powoduje zaktualizowanie reguły zapory MySql na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="8d396-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="8d396-114">Przykład 2: aktualizowanie reguły zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="8d396-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="8d396-115">Te polecenia cmdlet aktualizują regułę zapory MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="8d396-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="8d396-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d396-116">PARAMETERS</span></span>

### <span data-ttu-id="8d396-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d396-117">-AsJob</span></span>
<span data-ttu-id="8d396-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8d396-118">Run the command as a job</span></span>

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

### <span data-ttu-id="8d396-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="8d396-119">-ClientIPAddress</span></span>
<span data-ttu-id="8d396-120">Klient określił jeden adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8d396-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="8d396-121">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="8d396-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="8d396-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d396-122">-DefaultProfile</span></span>
<span data-ttu-id="8d396-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d396-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d396-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="8d396-124">-EndIPAddress</span></span>
<span data-ttu-id="8d396-125">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8d396-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="8d396-126">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="8d396-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="8d396-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8d396-127">-InputObject</span></span>
<span data-ttu-id="8d396-128">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8d396-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d396-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8d396-129">-Name</span></span>
<span data-ttu-id="8d396-130">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8d396-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="8d396-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8d396-131">-NoWait</span></span>
<span data-ttu-id="8d396-132">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8d396-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8d396-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d396-133">-ResourceGroupName</span></span>
<span data-ttu-id="8d396-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d396-134">The name of the resource group.</span></span>
<span data-ttu-id="8d396-135">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8d396-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8d396-136">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8d396-136">-ServerName</span></span>
<span data-ttu-id="8d396-137">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8d396-137">The name of the server.</span></span>

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

### <span data-ttu-id="8d396-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="8d396-138">-StartIPAddress</span></span>
<span data-ttu-id="8d396-139">Początkowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8d396-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="8d396-140">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="8d396-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="8d396-141">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8d396-141">-SubscriptionId</span></span>
<span data-ttu-id="8d396-142">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8d396-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8d396-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d396-143">-Confirm</span></span>
<span data-ttu-id="8d396-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d396-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d396-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d396-145">-WhatIf</span></span>
<span data-ttu-id="8d396-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d396-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d396-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8d396-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d396-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d396-148">CommonParameters</span></span>
<span data-ttu-id="8d396-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d396-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d396-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d396-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d396-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d396-151">INPUTS</span></span>

### <span data-ttu-id="8d396-152">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8d396-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8d396-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d396-153">OUTPUTS</span></span>

### <span data-ttu-id="8d396-154">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8d396-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="8d396-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d396-155">NOTES</span></span>

<span data-ttu-id="8d396-156">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8d396-156">ALIASES</span></span>

<span data-ttu-id="8d396-157">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d396-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d396-158">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8d396-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d396-159">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d396-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d396-160">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="8d396-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d396-161">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="8d396-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8d396-162">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8d396-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8d396-163">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8d396-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8d396-164">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8d396-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d396-165">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="8d396-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="8d396-166">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8d396-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8d396-167">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d396-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8d396-168">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8d396-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d396-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="8d396-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8d396-170">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8d396-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8d396-171">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8d396-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8d396-172">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d396-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8d396-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d396-173">RELATED LINKS</span></span>

