---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340573"
---
# <span data-ttu-id="0d43f-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0d43f-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="0d43f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d43f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d43f-103">Pobiera informacje dotyczące reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0d43f-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="0d43f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d43f-104">SYNTAX</span></span>

### <span data-ttu-id="0d43f-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0d43f-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d43f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="0d43f-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d43f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d43f-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d43f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0d43f-108">DESCRIPTION</span></span>
<span data-ttu-id="0d43f-109">Pobiera informacje dotyczące reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0d43f-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="0d43f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d43f-110">EXAMPLES</span></span>

### <span data-ttu-id="0d43f-111">Przykład 1: wyświetla wszystkie reguły zapory na określonym serwerze PostgreSql</span><span class="sxs-lookup"><span data-stu-id="0d43f-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="0d43f-112">To polecenie cmdlet wyświetla listę wszystkich reguł zapory na określonym serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="0d43f-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="0d43f-113">Przykład 2: uzyskiwanie reguły zapory według nazwy</span><span class="sxs-lookup"><span data-stu-id="0d43f-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="0d43f-114">To polecenie cmdlet umożliwia pobieranie reguły zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0d43f-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="0d43f-115">Przykład 3: uzyskiwanie reguły zapory według tożsamości</span><span class="sxs-lookup"><span data-stu-id="0d43f-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="0d43f-116">To polecenie cmdlet umożliwia pobieranie reguły zapory według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="0d43f-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="0d43f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d43f-117">PARAMETERS</span></span>

### <span data-ttu-id="0d43f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d43f-118">-DefaultProfile</span></span>
<span data-ttu-id="0d43f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d43f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d43f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d43f-120">-InputObject</span></span>
<span data-ttu-id="0d43f-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0d43f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0d43f-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d43f-122">-Name</span></span>
<span data-ttu-id="0d43f-123">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0d43f-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="0d43f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d43f-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d43f-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d43f-125">The name of the resource group.</span></span>
<span data-ttu-id="0d43f-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0d43f-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0d43f-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0d43f-127">-ServerName</span></span>
<span data-ttu-id="0d43f-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0d43f-128">The name of the server.</span></span>

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

### <span data-ttu-id="0d43f-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0d43f-129">-SubscriptionId</span></span>
<span data-ttu-id="0d43f-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0d43f-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0d43f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d43f-131">CommonParameters</span></span>
<span data-ttu-id="0d43f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d43f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d43f-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d43f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d43f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d43f-134">INPUTS</span></span>

### <span data-ttu-id="0d43f-135">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0d43f-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0d43f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d43f-136">OUTPUTS</span></span>

### <span data-ttu-id="0d43f-137">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0d43f-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="0d43f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d43f-138">NOTES</span></span>

<span data-ttu-id="0d43f-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0d43f-139">ALIASES</span></span>

<span data-ttu-id="0d43f-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d43f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d43f-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0d43f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d43f-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d43f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d43f-143">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="0d43f-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d43f-144">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="0d43f-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0d43f-145">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0d43f-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0d43f-146">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0d43f-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0d43f-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0d43f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d43f-148">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0d43f-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0d43f-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d43f-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0d43f-150">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0d43f-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="0d43f-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="0d43f-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0d43f-152">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0d43f-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0d43f-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0d43f-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0d43f-154">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0d43f-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0d43f-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d43f-155">RELATED LINKS</span></span>

