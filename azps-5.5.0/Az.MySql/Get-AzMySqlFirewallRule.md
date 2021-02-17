---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: f750718c4bd380b579dff0897b53a68ae4f45b95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192147"
---
# <span data-ttu-id="f1b51-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f1b51-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="f1b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1b51-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b51-103">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f1b51-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="f1b51-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1b51-104">SYNTAX</span></span>

### <span data-ttu-id="f1b51-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f1b51-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f1b51-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f1b51-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f1b51-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1b51-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f1b51-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1b51-108">DESCRIPTION</span></span>
<span data-ttu-id="f1b51-109">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f1b51-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="f1b51-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1b51-110">EXAMPLES</span></span>

### <span data-ttu-id="f1b51-111">Przykład 1. Lista wszystkich reguł zapory na określonym serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="f1b51-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="f1b51-112">To polecenie cmdlet wyświetla listę wszystkich reguł zapory na określonym serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="f1b51-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="f1b51-113">Przykład 2. Uzyskiwanie reguły zapory według nazwy</span><span class="sxs-lookup"><span data-stu-id="f1b51-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="f1b51-114">To polecenie cmdlet pobiera regułę zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f1b51-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="f1b51-115">Przykład 3. Uzyskiwanie reguły zapory według tożsamości</span><span class="sxs-lookup"><span data-stu-id="f1b51-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="f1b51-116">To polecenie cmdlet pobiera regułę zapory przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="f1b51-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="f1b51-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1b51-117">PARAMETERS</span></span>

### <span data-ttu-id="f1b51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b51-118">-DefaultProfile</span></span>
<span data-ttu-id="f1b51-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b51-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1b51-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1b51-120">-InputObject</span></span>
<span data-ttu-id="f1b51-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f1b51-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b51-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f1b51-122">-Name</span></span>
<span data-ttu-id="f1b51-123">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f1b51-123">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b51-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b51-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1b51-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f1b51-125">The name of the resource group.</span></span>
<span data-ttu-id="f1b51-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f1b51-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b51-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f1b51-127">-ServerName</span></span>
<span data-ttu-id="f1b51-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f1b51-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b51-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1b51-129">-SubscriptionId</span></span>
<span data-ttu-id="f1b51-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f1b51-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b51-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b51-131">CommonParameters</span></span>
<span data-ttu-id="f1b51-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b51-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b51-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1b51-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b51-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1b51-134">INPUTS</span></span>

### <span data-ttu-id="f1b51-135">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f1b51-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f1b51-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1b51-136">OUTPUTS</span></span>

### <span data-ttu-id="f1b51-137">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f1b51-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="f1b51-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1b51-138">NOTES</span></span>

<span data-ttu-id="f1b51-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f1b51-139">ALIASES</span></span>

<span data-ttu-id="f1b51-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f1b51-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1b51-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f1b51-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1b51-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1b51-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1b51-143">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="f1b51-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1b51-144">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="f1b51-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f1b51-145">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f1b51-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f1b51-146">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f1b51-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f1b51-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f1b51-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1b51-148">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="f1b51-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="f1b51-149">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f1b51-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f1b51-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f1b51-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f1b51-151">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f1b51-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="f1b51-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f1b51-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f1b51-153">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f1b51-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f1b51-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f1b51-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f1b51-155">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f1b51-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f1b51-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1b51-156">RELATED LINKS</span></span>

