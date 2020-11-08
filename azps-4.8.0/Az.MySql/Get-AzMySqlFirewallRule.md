---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: 11278c1d317f6f4e0171513a4503c5681506f1ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222444"
---
# <span data-ttu-id="ba6dd-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ba6dd-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="ba6dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6dd-103">Pobiera informacje dotyczące reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="ba6dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba6dd-104">SYNTAX</span></span>

### <span data-ttu-id="ba6dd-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ba6dd-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ba6dd-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ba6dd-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ba6dd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ba6dd-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ba6dd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ba6dd-108">DESCRIPTION</span></span>
<span data-ttu-id="ba6dd-109">Pobiera informacje dotyczące reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="ba6dd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba6dd-110">EXAMPLES</span></span>

### <span data-ttu-id="ba6dd-111">Przykład 1: Lista wszystkich reguł zapory w określonym serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="ba6dd-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="ba6dd-112">To polecenie cmdlet wyświetla listę wszystkich reguł zapory określonych w serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="ba6dd-113">Przykład 2: uzyskiwanie reguły zapory według nazwy</span><span class="sxs-lookup"><span data-stu-id="ba6dd-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="ba6dd-114">To polecenie cmdlet umożliwia pobieranie reguły zapory według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="ba6dd-115">Przykład 3: uzyskiwanie reguły zapory według tożsamości</span><span class="sxs-lookup"><span data-stu-id="ba6dd-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="ba6dd-116">To polecenie cmdlet umożliwia pobieranie reguły zapory według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="ba6dd-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba6dd-117">PARAMETERS</span></span>

### <span data-ttu-id="ba6dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6dd-118">-DefaultProfile</span></span>
<span data-ttu-id="ba6dd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba6dd-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ba6dd-120">-InputObject</span></span>
<span data-ttu-id="ba6dd-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba6dd-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba6dd-122">-Name</span></span>
<span data-ttu-id="ba6dd-123">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="ba6dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba6dd-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-125">The name of the resource group.</span></span>
<span data-ttu-id="ba6dd-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ba6dd-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ba6dd-127">-ServerName</span></span>
<span data-ttu-id="ba6dd-128">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-128">The name of the server.</span></span>

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

### <span data-ttu-id="ba6dd-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ba6dd-129">-SubscriptionId</span></span>
<span data-ttu-id="ba6dd-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ba6dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6dd-131">CommonParameters</span></span>
<span data-ttu-id="ba6dd-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6dd-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba6dd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6dd-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba6dd-134">INPUTS</span></span>

### <span data-ttu-id="ba6dd-135">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ba6dd-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ba6dd-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba6dd-136">OUTPUTS</span></span>

### <span data-ttu-id="ba6dd-137">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ba6dd-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="ba6dd-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba6dd-138">NOTES</span></span>

<span data-ttu-id="ba6dd-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ba6dd-139">ALIASES</span></span>

<span data-ttu-id="ba6dd-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba6dd-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba6dd-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba6dd-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba6dd-143">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ba6dd-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba6dd-144">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ba6dd-145">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ba6dd-146">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ba6dd-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ba6dd-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba6dd-148">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ba6dd-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ba6dd-150">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="ba6dd-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ba6dd-152">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ba6dd-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ba6dd-154">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ba6dd-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba6dd-155">RELATED LINKS</span></span>

