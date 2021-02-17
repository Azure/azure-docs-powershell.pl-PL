---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189378"
---
# <span data-ttu-id="f8fe9-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f8fe9-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="f8fe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fe9-103">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="f8fe9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f8fe9-104">SYNTAX</span></span>

### <span data-ttu-id="f8fe9-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f8fe9-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8fe9-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f8fe9-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f8fe9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f8fe9-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8fe9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f8fe9-108">DESCRIPTION</span></span>
<span data-ttu-id="f8fe9-109">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="f8fe9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f8fe9-110">EXAMPLES</span></span>

### <span data-ttu-id="f8fe9-111">Przykład 1. Lista wszystkich reguł zapory na określonym serwerze PostgreSql</span><span class="sxs-lookup"><span data-stu-id="f8fe9-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="f8fe9-112">To polecenie cmdlet wyświetla listę wszystkich reguł zapory na określonym serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="f8fe9-113">Przykład 2. Uzyskiwanie reguły zapory według nazwy</span><span class="sxs-lookup"><span data-stu-id="f8fe9-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="f8fe9-114">To polecenie cmdlet pobiera regułę zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="f8fe9-115">Przykład 3. Uzyskiwanie reguły zapory według tożsamości</span><span class="sxs-lookup"><span data-stu-id="f8fe9-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="f8fe9-116">To polecenie cmdlet pobiera regułę zapory za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="f8fe9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8fe9-117">PARAMETERS</span></span>

### <span data-ttu-id="f8fe9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fe9-118">-DefaultProfile</span></span>
<span data-ttu-id="f8fe9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8fe9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8fe9-120">-InputObject</span></span>
<span data-ttu-id="f8fe9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f8fe9-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f8fe9-122">-Name</span></span>
<span data-ttu-id="f8fe9-123">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="f8fe9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8fe9-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8fe9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-125">The name of the resource group.</span></span>
<span data-ttu-id="f8fe9-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f8fe9-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f8fe9-127">-ServerName</span></span>
<span data-ttu-id="f8fe9-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-128">The name of the server.</span></span>

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

### <span data-ttu-id="f8fe9-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8fe9-129">-SubscriptionId</span></span>
<span data-ttu-id="f8fe9-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f8fe9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fe9-131">CommonParameters</span></span>
<span data-ttu-id="f8fe9-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fe9-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8fe9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fe9-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8fe9-134">INPUTS</span></span>

### <span data-ttu-id="f8fe9-135">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f8fe9-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="f8fe9-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8fe9-136">OUTPUTS</span></span>

### <span data-ttu-id="f8fe9-137">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f8fe9-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="f8fe9-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f8fe9-138">NOTES</span></span>

<span data-ttu-id="f8fe9-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f8fe9-139">ALIASES</span></span>

<span data-ttu-id="f8fe9-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f8fe9-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8fe9-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8fe9-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8fe9-143">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="f8fe9-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8fe9-144">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f8fe9-145">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f8fe9-146">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f8fe9-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f8fe9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8fe9-148">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f8fe9-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f8fe9-150">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="f8fe9-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f8fe9-152">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f8fe9-153">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f8fe9-154">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f8fe9-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f8fe9-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8fe9-155">RELATED LINKS</span></span>

