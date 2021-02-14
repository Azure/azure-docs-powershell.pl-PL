---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 7f2a3e567da4df9a004c5dac642f480a4cd7388a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190043"
---
# <span data-ttu-id="b4ff2-101">Get-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4ff2-101">Get-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="b4ff2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ff2-103">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="b4ff2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4ff2-104">SYNTAX</span></span>

### <span data-ttu-id="b4ff2-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b4ff2-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4ff2-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b4ff2-106">Get</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4ff2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b4ff2-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4ff2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4ff2-108">DESCRIPTION</span></span>
<span data-ttu-id="b4ff2-109">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="b4ff2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4ff2-110">EXAMPLES</span></span>

### <span data-ttu-id="b4ff2-111">Przykład 1. Uzyskiwanie reguł zapory według nazwy</span><span class="sxs-lookup"><span data-stu-id="b4ff2-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="b4ff2-112">To polecenie cmdlet pobiera reguły zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="b4ff2-113">Przykład 2. Uzyskiwanie reguł zapory według tożsamości</span><span class="sxs-lookup"><span data-stu-id="b4ff2-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="b4ff2-114">To polecenie cmdlet pobiera reguły zapory według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="b4ff2-115">Przykład 3. Lista wszystkich reguł zapory na określonym serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="b4ff2-115">Example 3: Lists all the firewall rules in the specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="b4ff2-116">To polecenie cmdlet wyświetla listę wszystkich reguł zapory na określonym serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-116">This cmdlet lists all the firewall rule in specified MySql server.</span></span>

## <span data-ttu-id="b4ff2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4ff2-117">PARAMETERS</span></span>

### <span data-ttu-id="b4ff2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ff2-118">-DefaultProfile</span></span>
<span data-ttu-id="b4ff2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ff2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4ff2-120">-InputObject</span></span>
<span data-ttu-id="b4ff2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4ff2-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b4ff2-122">-Name</span></span>
<span data-ttu-id="b4ff2-123">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b4ff2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ff2-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4ff2-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-125">The name of the resource group.</span></span>
<span data-ttu-id="b4ff2-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b4ff2-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4ff2-127">-ServerName</span></span>
<span data-ttu-id="b4ff2-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-128">The name of the server.</span></span>

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

### <span data-ttu-id="b4ff2-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4ff2-129">-SubscriptionId</span></span>
<span data-ttu-id="b4ff2-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b4ff2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ff2-131">CommonParameters</span></span>
<span data-ttu-id="b4ff2-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ff2-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4ff2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ff2-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4ff2-134">INPUTS</span></span>

### <span data-ttu-id="b4ff2-135">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b4ff2-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b4ff2-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4ff2-136">OUTPUTS</span></span>

### <span data-ttu-id="b4ff2-137">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4ff2-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="b4ff2-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4ff2-138">NOTES</span></span>

<span data-ttu-id="b4ff2-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b4ff2-139">ALIASES</span></span>

<span data-ttu-id="b4ff2-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4ff2-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b4ff2-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4ff2-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b4ff2-143">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b4ff2-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b4ff2-144">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b4ff2-145">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b4ff2-146">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b4ff2-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b4ff2-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b4ff2-148">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b4ff2-149">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b4ff2-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b4ff2-151">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="b4ff2-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b4ff2-153">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b4ff2-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b4ff2-155">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b4ff2-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4ff2-156">RELATED LINKS</span></span>

