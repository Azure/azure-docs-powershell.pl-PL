---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: ecd254c26aba19b99e046efb88c7651d007ae05f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967761"
---
# <span data-ttu-id="ae75c-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae75c-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="ae75c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae75c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae75c-103">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ae75c-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="ae75c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae75c-104">SYNTAX</span></span>

### <span data-ttu-id="ae75c-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ae75c-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ae75c-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ae75c-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ae75c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ae75c-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae75c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae75c-108">DESCRIPTION</span></span>
<span data-ttu-id="ae75c-109">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ae75c-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="ae75c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae75c-110">EXAMPLES</span></span>

### <span data-ttu-id="ae75c-111">Przykład 1. Lista wszystkich reguł zapory na określonym serwerze PostgreSql</span><span class="sxs-lookup"><span data-stu-id="ae75c-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="ae75c-112">To polecenie cmdlet wyświetla listę wszystkich reguł zapory na określonym serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="ae75c-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="ae75c-113">Przykład 2. Uzyskiwanie reguły zapory według nazwy</span><span class="sxs-lookup"><span data-stu-id="ae75c-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="ae75c-114">To polecenie cmdlet pobiera regułę zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ae75c-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="ae75c-115">Przykład 3. Uzyskiwanie reguły zapory według tożsamości</span><span class="sxs-lookup"><span data-stu-id="ae75c-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="ae75c-116">To polecenie cmdlet pobiera regułę zapory przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="ae75c-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="ae75c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae75c-117">PARAMETERS</span></span>

### <span data-ttu-id="ae75c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae75c-118">-DefaultProfile</span></span>
<span data-ttu-id="ae75c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae75c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae75c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae75c-120">-InputObject</span></span>
<span data-ttu-id="ae75c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ae75c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ae75c-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae75c-122">-Name</span></span>
<span data-ttu-id="ae75c-123">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ae75c-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="ae75c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae75c-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae75c-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae75c-125">The name of the resource group.</span></span>
<span data-ttu-id="ae75c-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ae75c-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ae75c-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ae75c-127">-ServerName</span></span>
<span data-ttu-id="ae75c-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ae75c-128">The name of the server.</span></span>

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

### <span data-ttu-id="ae75c-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae75c-129">-SubscriptionId</span></span>
<span data-ttu-id="ae75c-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ae75c-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ae75c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae75c-131">CommonParameters</span></span>
<span data-ttu-id="ae75c-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae75c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae75c-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae75c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae75c-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae75c-134">INPUTS</span></span>

### <span data-ttu-id="ae75c-135">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ae75c-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="ae75c-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae75c-136">OUTPUTS</span></span>

### <span data-ttu-id="ae75c-137">Microsoft.Azure.PowerShell.cmdlet.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae75c-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="ae75c-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae75c-138">NOTES</span></span>

<span data-ttu-id="ae75c-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ae75c-139">ALIASES</span></span>

<span data-ttu-id="ae75c-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae75c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae75c-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ae75c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae75c-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ae75c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae75c-143">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ae75c-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ae75c-144">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="ae75c-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ae75c-145">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ae75c-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ae75c-146">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ae75c-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ae75c-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ae75c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ae75c-148">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ae75c-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ae75c-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae75c-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ae75c-150">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ae75c-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="ae75c-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ae75c-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ae75c-152">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ae75c-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ae75c-153">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ae75c-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ae75c-154">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae75c-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ae75c-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae75c-155">RELATED LINKS</span></span>

