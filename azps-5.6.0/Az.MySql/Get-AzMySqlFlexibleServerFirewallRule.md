---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: e52e4b0a8c5d18b5746a604410b6ec909782ec9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012881"
---
# <span data-ttu-id="e2ff9-101">Get-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e2ff9-101">Get-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="e2ff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ff9-103">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="e2ff9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e2ff9-104">SYNTAX</span></span>

### <span data-ttu-id="e2ff9-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e2ff9-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e2ff9-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e2ff9-106">Get</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e2ff9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e2ff9-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2ff9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e2ff9-108">DESCRIPTION</span></span>
<span data-ttu-id="e2ff9-109">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="e2ff9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e2ff9-110">EXAMPLES</span></span>

### <span data-ttu-id="e2ff9-111">Przykład 1. Uzyskiwanie reguł zapory według nazwy</span><span class="sxs-lookup"><span data-stu-id="e2ff9-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="e2ff9-112">To polecenie cmdlet otrzymuje reguły zapory według nazw.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="e2ff9-113">Przykład 2. Uzyskiwanie reguł zapory według tożsamości</span><span class="sxs-lookup"><span data-stu-id="e2ff9-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="e2ff9-114">To polecenie cmdlet pobiera reguły zapory według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="e2ff9-115">Przykład 3. Lista wszystkich reguł zapory na określonym serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="e2ff9-115">Example 3: Lists all the firewall rules in the specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="e2ff9-116">To polecenie cmdlet wyświetla listę wszystkich reguł zapory na określonym serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-116">This cmdlet lists all the firewall rule in specified MySql server.</span></span>

## <span data-ttu-id="e2ff9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2ff9-117">PARAMETERS</span></span>

### <span data-ttu-id="e2ff9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ff9-118">-DefaultProfile</span></span>
<span data-ttu-id="e2ff9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2ff9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2ff9-120">-InputObject</span></span>
<span data-ttu-id="e2ff9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e2ff9-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e2ff9-122">-Name</span></span>
<span data-ttu-id="e2ff9-123">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="e2ff9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ff9-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2ff9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-125">The name of the resource group.</span></span>
<span data-ttu-id="e2ff9-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e2ff9-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e2ff9-127">-ServerName</span></span>
<span data-ttu-id="e2ff9-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-128">The name of the server.</span></span>

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

### <span data-ttu-id="e2ff9-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2ff9-129">-SubscriptionId</span></span>
<span data-ttu-id="e2ff9-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e2ff9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ff9-131">CommonParameters</span></span>
<span data-ttu-id="e2ff9-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ff9-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2ff9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ff9-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2ff9-134">INPUTS</span></span>

### <span data-ttu-id="e2ff9-135">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e2ff9-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="e2ff9-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2ff9-136">OUTPUTS</span></span>

### <span data-ttu-id="e2ff9-137">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e2ff9-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="e2ff9-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e2ff9-138">NOTES</span></span>

<span data-ttu-id="e2ff9-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e2ff9-139">ALIASES</span></span>

<span data-ttu-id="e2ff9-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2ff9-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2ff9-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2ff9-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2ff9-143">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e2ff9-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2ff9-144">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e2ff9-145">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e2ff9-146">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e2ff9-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e2ff9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2ff9-148">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="e2ff9-149">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e2ff9-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e2ff9-151">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="e2ff9-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e2ff9-153">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e2ff9-154">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e2ff9-155">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2ff9-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e2ff9-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2ff9-156">RELATED LINKS</span></span>

