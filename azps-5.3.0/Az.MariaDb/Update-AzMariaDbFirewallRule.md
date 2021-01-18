---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500766"
---
# <span data-ttu-id="efb03-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="efb03-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="efb03-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="efb03-102">SYNOPSIS</span></span>
<span data-ttu-id="efb03-103">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="efb03-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="efb03-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="efb03-104">SYNTAX</span></span>

### <span data-ttu-id="efb03-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="efb03-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="efb03-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="efb03-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="efb03-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="efb03-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="efb03-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="efb03-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="efb03-109">Opis</span><span class="sxs-lookup"><span data-stu-id="efb03-109">DESCRIPTION</span></span>
<span data-ttu-id="efb03-110">Powoduje utworzenie nowej reguły zapory lub zaktualizowanie istniejącej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="efb03-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="efb03-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="efb03-111">EXAMPLES</span></span>

### <span data-ttu-id="efb03-112">Przykład 1: aktualizowanie reguły zapory MariaDB</span><span class="sxs-lookup"><span data-stu-id="efb03-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="efb03-113">To polecenie aktualizuje regułę zapory MariaDB.</span><span class="sxs-lookup"><span data-stu-id="efb03-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="efb03-114">Przykład 2: aktualizowanie reguły zapory MariaDB według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="efb03-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="efb03-115">Polecenie cmdlet aktualizuje MariaDBą regułę zapory według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="efb03-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="efb03-116">Przykład 3: aktualizowanie reguły zapory MariaDB przez-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="efb03-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="efb03-117">Polecenie cmdlet aktualizuje MariaDBą regułę zapory o-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="efb03-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="efb03-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="efb03-118">PARAMETERS</span></span>

### <span data-ttu-id="efb03-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efb03-119">-AsJob</span></span>
<span data-ttu-id="efb03-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="efb03-120">Run the command as a job</span></span>

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

### <span data-ttu-id="efb03-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="efb03-121">-ClientIPAddress</span></span>
<span data-ttu-id="efb03-122">Klient określił jeden adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="efb03-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="efb03-123">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="efb03-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="efb03-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb03-124">-DefaultProfile</span></span>
<span data-ttu-id="efb03-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="efb03-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efb03-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="efb03-126">-EndIPAddress</span></span>
<span data-ttu-id="efb03-127">Końcowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="efb03-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="efb03-128">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="efb03-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="efb03-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="efb03-129">-InputObject</span></span>
<span data-ttu-id="efb03-130">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="efb03-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efb03-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="efb03-131">-Name</span></span>
<span data-ttu-id="efb03-132">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="efb03-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="efb03-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="efb03-133">-NoWait</span></span>
<span data-ttu-id="efb03-134">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="efb03-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="efb03-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb03-135">-ResourceGroupName</span></span>
<span data-ttu-id="efb03-136">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="efb03-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="efb03-137">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="efb03-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="efb03-138">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="efb03-138">-ServerName</span></span>
<span data-ttu-id="efb03-139">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="efb03-139">The name of the server.</span></span>

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

### <span data-ttu-id="efb03-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="efb03-140">-StartIPAddress</span></span>
<span data-ttu-id="efb03-141">Początkowy adres IP reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="efb03-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="efb03-142">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="efb03-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="efb03-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="efb03-143">-SubscriptionId</span></span>
<span data-ttu-id="efb03-144">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="efb03-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="efb03-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efb03-145">-Confirm</span></span>
<span data-ttu-id="efb03-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efb03-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efb03-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb03-147">-WhatIf</span></span>
<span data-ttu-id="efb03-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efb03-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efb03-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="efb03-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efb03-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb03-150">CommonParameters</span></span>
<span data-ttu-id="efb03-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb03-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb03-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efb03-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb03-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efb03-153">INPUTS</span></span>

### <span data-ttu-id="efb03-154">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="efb03-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="efb03-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="efb03-155">OUTPUTS</span></span>

### <span data-ttu-id="efb03-156">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="efb03-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="efb03-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="efb03-157">NOTES</span></span>

<span data-ttu-id="efb03-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="efb03-158">ALIASES</span></span>

<span data-ttu-id="efb03-159">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="efb03-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="efb03-160">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="efb03-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="efb03-161">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="efb03-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="efb03-162">INPUTobject <IMariaDbIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="efb03-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="efb03-163">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="efb03-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="efb03-164">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="efb03-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="efb03-165">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="efb03-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="efb03-166">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="efb03-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="efb03-167">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="efb03-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="efb03-168">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="efb03-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="efb03-169">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="efb03-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="efb03-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="efb03-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="efb03-171">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="efb03-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="efb03-172">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="efb03-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="efb03-173">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="efb03-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="efb03-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efb03-174">RELATED LINKS</span></span>

