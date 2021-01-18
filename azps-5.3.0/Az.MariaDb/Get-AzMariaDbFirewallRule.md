---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500810"
---
# <span data-ttu-id="29027-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="29027-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="29027-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29027-102">SYNOPSIS</span></span>
<span data-ttu-id="29027-103">Pobiera informacje dotyczące reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="29027-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="29027-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29027-104">SYNTAX</span></span>

### <span data-ttu-id="29027-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="29027-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="29027-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="29027-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="29027-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="29027-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="29027-108">Opis</span><span class="sxs-lookup"><span data-stu-id="29027-108">DESCRIPTION</span></span>
<span data-ttu-id="29027-109">Pobiera informacje dotyczące reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="29027-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="29027-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29027-110">EXAMPLES</span></span>

### <span data-ttu-id="29027-111">Przykład 1: wyświetlanie wszystkich reguł zapory pod MariaDB</span><span class="sxs-lookup"><span data-stu-id="29027-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="29027-112">To polecenie wyświetla listę wszystkich reguł girewall pod MariaDB.</span><span class="sxs-lookup"><span data-stu-id="29027-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="29027-113">Przykład 2: uzyskiwanie reguły zapory w obszarze MariaDB</span><span class="sxs-lookup"><span data-stu-id="29027-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="29027-114">To polecenie pobiera regułę zapory pod MariaDB.</span><span class="sxs-lookup"><span data-stu-id="29027-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="29027-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29027-115">PARAMETERS</span></span>

### <span data-ttu-id="29027-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29027-116">-DefaultProfile</span></span>
<span data-ttu-id="29027-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29027-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29027-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29027-118">-InputObject</span></span>
<span data-ttu-id="29027-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="29027-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29027-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29027-120">-Name</span></span>
<span data-ttu-id="29027-121">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="29027-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="29027-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29027-122">-ResourceGroupName</span></span>
<span data-ttu-id="29027-123">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="29027-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="29027-124">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="29027-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="29027-125">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="29027-125">-ServerName</span></span>
<span data-ttu-id="29027-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="29027-126">The name of the server.</span></span>

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

### <span data-ttu-id="29027-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="29027-127">-SubscriptionId</span></span>
<span data-ttu-id="29027-128">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="29027-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="29027-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29027-129">CommonParameters</span></span>
<span data-ttu-id="29027-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29027-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29027-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29027-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29027-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29027-132">INPUTS</span></span>

### <span data-ttu-id="29027-133">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="29027-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="29027-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29027-134">OUTPUTS</span></span>

### <span data-ttu-id="29027-135">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="29027-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="29027-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29027-136">NOTES</span></span>

<span data-ttu-id="29027-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="29027-137">ALIASES</span></span>

<span data-ttu-id="29027-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29027-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="29027-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="29027-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29027-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="29027-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="29027-141">INPUTobject <IMariaDbIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="29027-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29027-142">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="29027-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="29027-143">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="29027-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="29027-144">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="29027-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="29027-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="29027-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29027-146">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="29027-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="29027-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="29027-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="29027-148">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="29027-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="29027-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="29027-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="29027-150">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="29027-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="29027-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="29027-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="29027-152">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="29027-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="29027-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29027-153">RELATED LINKS</span></span>

