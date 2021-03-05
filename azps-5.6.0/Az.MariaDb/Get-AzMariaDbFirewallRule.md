---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 1c7b3c1f64637554745e960fadfe93cb3d87fa84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994176"
---
# <span data-ttu-id="be4d4-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="be4d4-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="be4d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="be4d4-103">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="be4d4-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="be4d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be4d4-104">SYNTAX</span></span>

### <span data-ttu-id="be4d4-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="be4d4-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="be4d4-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="be4d4-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="be4d4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="be4d4-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="be4d4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="be4d4-108">DESCRIPTION</span></span>
<span data-ttu-id="be4d4-109">Pobiera informacje na temat reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="be4d4-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="be4d4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be4d4-110">EXAMPLES</span></span>

### <span data-ttu-id="be4d4-111">Przykład 1. Lista wszystkich reguł zapory w obszarze bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="be4d4-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="be4d4-112">To polecenie wyświetla listę wszystkich reguł girewall w obszarze MariaDB.</span><span class="sxs-lookup"><span data-stu-id="be4d4-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="be4d4-113">Przykład 2. Uzyskiwanie reguły zapory w obszarze bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="be4d4-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="be4d4-114">To polecenie pobiera regułę zapory w obszarze bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="be4d4-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="be4d4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be4d4-115">PARAMETERS</span></span>

### <span data-ttu-id="be4d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be4d4-116">-DefaultProfile</span></span>
<span data-ttu-id="be4d4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="be4d4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be4d4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be4d4-118">-InputObject</span></span>
<span data-ttu-id="be4d4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="be4d4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="be4d4-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="be4d4-120">-Name</span></span>
<span data-ttu-id="be4d4-121">Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="be4d4-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="be4d4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be4d4-122">-ResourceGroupName</span></span>
<span data-ttu-id="be4d4-123">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="be4d4-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="be4d4-124">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="be4d4-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="be4d4-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="be4d4-125">-ServerName</span></span>
<span data-ttu-id="be4d4-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="be4d4-126">The name of the server.</span></span>

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

### <span data-ttu-id="be4d4-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be4d4-127">-SubscriptionId</span></span>
<span data-ttu-id="be4d4-128">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="be4d4-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="be4d4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be4d4-129">CommonParameters</span></span>
<span data-ttu-id="be4d4-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be4d4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be4d4-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be4d4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be4d4-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be4d4-132">INPUTS</span></span>

### <span data-ttu-id="be4d4-133">Microsoft.Azure.PowerShell.Cmdlet.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="be4d4-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="be4d4-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be4d4-134">OUTPUTS</span></span>

### <span data-ttu-id="be4d4-135">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="be4d4-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="be4d4-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be4d4-136">NOTES</span></span>

<span data-ttu-id="be4d4-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="be4d4-137">ALIASES</span></span>

<span data-ttu-id="be4d4-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be4d4-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be4d4-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="be4d4-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be4d4-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be4d4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be4d4-141">INPUTOBJECT: <IMariaDbIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="be4d4-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be4d4-142">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="be4d4-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="be4d4-143">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="be4d4-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="be4d4-144">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="be4d4-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="be4d4-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="be4d4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be4d4-146">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="be4d4-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="be4d4-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="be4d4-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="be4d4-148">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="be4d4-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="be4d4-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="be4d4-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="be4d4-150">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="be4d4-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="be4d4-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="be4d4-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="be4d4-152">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="be4d4-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="be4d4-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be4d4-153">RELATED LINKS</span></span>

