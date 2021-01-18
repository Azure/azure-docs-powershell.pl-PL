---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 7f2a3e567da4df9a004c5dac642f480a4cd7388a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503292"
---
# <span data-ttu-id="806ad-101">Get-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="806ad-101">Get-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="806ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="806ad-102">SYNOPSIS</span></span>
<span data-ttu-id="806ad-103">Pobiera informacje dotyczące reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="806ad-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="806ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="806ad-104">SYNTAX</span></span>

### <span data-ttu-id="806ad-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="806ad-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="806ad-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="806ad-106">Get</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="806ad-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="806ad-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="806ad-108">Opis</span><span class="sxs-lookup"><span data-stu-id="806ad-108">DESCRIPTION</span></span>
<span data-ttu-id="806ad-109">Pobiera informacje dotyczące reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="806ad-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="806ad-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="806ad-110">EXAMPLES</span></span>

### <span data-ttu-id="806ad-111">Przykład 1: Uzyskaj reguły zapory według nazwy</span><span class="sxs-lookup"><span data-stu-id="806ad-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="806ad-112">To polecenie cmdlet umożliwia pobieranie reguł zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="806ad-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="806ad-113">Przykład 2: uzyskiwanie reguł zapory według tożsamości</span><span class="sxs-lookup"><span data-stu-id="806ad-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="806ad-114">To polecenie cmdlet umożliwia pobieranie reguł zapory według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="806ad-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="806ad-115">Przykład 3: Lista wszystkich reguł zapory na określonym serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="806ad-115">Example 3: Lists all the firewall rules in the specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="806ad-116">To polecenie cmdlet wyświetla listę wszystkich reguł zapory określonych w serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="806ad-116">This cmdlet lists all the firewall rule in specified MySql server.</span></span>

## <span data-ttu-id="806ad-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="806ad-117">PARAMETERS</span></span>

### <span data-ttu-id="806ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806ad-118">-DefaultProfile</span></span>
<span data-ttu-id="806ad-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="806ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="806ad-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="806ad-120">-InputObject</span></span>
<span data-ttu-id="806ad-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="806ad-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="806ad-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="806ad-122">-Name</span></span>
<span data-ttu-id="806ad-123">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="806ad-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="806ad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="806ad-124">-ResourceGroupName</span></span>
<span data-ttu-id="806ad-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="806ad-125">The name of the resource group.</span></span>
<span data-ttu-id="806ad-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="806ad-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="806ad-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="806ad-127">-ServerName</span></span>
<span data-ttu-id="806ad-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="806ad-128">The name of the server.</span></span>

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

### <span data-ttu-id="806ad-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="806ad-129">-SubscriptionId</span></span>
<span data-ttu-id="806ad-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="806ad-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="806ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806ad-131">CommonParameters</span></span>
<span data-ttu-id="806ad-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="806ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806ad-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="806ad-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806ad-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="806ad-134">INPUTS</span></span>

### <span data-ttu-id="806ad-135">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="806ad-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="806ad-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="806ad-136">OUTPUTS</span></span>

### <span data-ttu-id="806ad-137">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="806ad-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="806ad-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="806ad-138">NOTES</span></span>

<span data-ttu-id="806ad-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="806ad-139">ALIASES</span></span>

<span data-ttu-id="806ad-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="806ad-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="806ad-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="806ad-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="806ad-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="806ad-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="806ad-143">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="806ad-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="806ad-144">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="806ad-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="806ad-145">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="806ad-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="806ad-146">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="806ad-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="806ad-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="806ad-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="806ad-148">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="806ad-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="806ad-149">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="806ad-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="806ad-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="806ad-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="806ad-151">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="806ad-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="806ad-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="806ad-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="806ad-153">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="806ad-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="806ad-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="806ad-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="806ad-155">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="806ad-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="806ad-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="806ad-156">RELATED LINKS</span></span>

