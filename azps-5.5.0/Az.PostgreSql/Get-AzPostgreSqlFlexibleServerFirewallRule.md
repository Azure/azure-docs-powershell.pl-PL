---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: a4b2f96644a2ec354b38dd13b159bb0f65f008c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179155"
---
# <span data-ttu-id="0bf9e-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0bf9e-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="0bf9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bf9e-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf9e-103">Lista wszystkich reguł zapory na danym serwerze.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-103">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="0bf9e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0bf9e-104">SYNTAX</span></span>

### <span data-ttu-id="0bf9e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0bf9e-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0bf9e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="0bf9e-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0bf9e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0bf9e-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bf9e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0bf9e-108">DESCRIPTION</span></span>
<span data-ttu-id="0bf9e-109">Lista wszystkich reguł zapory na danym serwerze.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-109">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="0bf9e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0bf9e-110">EXAMPLES</span></span>

### <span data-ttu-id="0bf9e-111">Przykład 1. Uzyskiwanie reguł zapory według nazwy</span><span class="sxs-lookup"><span data-stu-id="0bf9e-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="0bf9e-112">To polecenie cmdlet pobiera reguły zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="0bf9e-113">Przykład 2. Uzyskiwanie reguł zapory według tożsamości</span><span class="sxs-lookup"><span data-stu-id="0bf9e-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/servers/postgresql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="0bf9e-114">To polecenie cmdlet pobiera reguły zapory według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="0bf9e-115">Przykład 3. Lista wszystkich reguł zapory na określonym serwerze PostgreSql</span><span class="sxs-lookup"><span data-stu-id="0bf9e-115">Example 3: Lists all the firewall rules in the specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="0bf9e-116">To polecenie cmdlet wyświetla listę wszystkich reguł zapory na określonym serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-116">This cmdlet lists all the firewall rule in specified PostgreSql server.</span></span>

## <span data-ttu-id="0bf9e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bf9e-117">PARAMETERS</span></span>

### <span data-ttu-id="0bf9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf9e-118">-DefaultProfile</span></span>
<span data-ttu-id="0bf9e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bf9e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bf9e-120">-InputObject</span></span>
<span data-ttu-id="0bf9e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bf9e-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0bf9e-122">-Name</span></span>
<span data-ttu-id="0bf9e-123">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="0bf9e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bf9e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0bf9e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-125">The name of the resource group.</span></span>
<span data-ttu-id="0bf9e-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0bf9e-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0bf9e-127">-ServerName</span></span>
<span data-ttu-id="0bf9e-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-128">The name of the server.</span></span>

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

### <span data-ttu-id="0bf9e-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0bf9e-129">-SubscriptionId</span></span>
<span data-ttu-id="0bf9e-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0bf9e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf9e-131">CommonParameters</span></span>
<span data-ttu-id="0bf9e-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf9e-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bf9e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf9e-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bf9e-134">INPUTS</span></span>

### <span data-ttu-id="0bf9e-135">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0bf9e-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0bf9e-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bf9e-136">OUTPUTS</span></span>

### <span data-ttu-id="0bf9e-137">Microsoft.Azure.PowerShell.cmdlet.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0bf9e-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="0bf9e-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0bf9e-138">NOTES</span></span>

<span data-ttu-id="0bf9e-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0bf9e-139">ALIASES</span></span>

<span data-ttu-id="0bf9e-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0bf9e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0bf9e-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0bf9e-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0bf9e-143">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="0bf9e-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0bf9e-144">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0bf9e-145">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0bf9e-146">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0bf9e-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0bf9e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0bf9e-148">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0bf9e-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0bf9e-150">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="0bf9e-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0bf9e-152">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0bf9e-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0bf9e-154">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0bf9e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bf9e-155">RELATED LINKS</span></span>

