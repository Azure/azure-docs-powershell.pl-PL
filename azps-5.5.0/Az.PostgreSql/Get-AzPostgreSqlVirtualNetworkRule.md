---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179139"
---
# <span data-ttu-id="8262e-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8262e-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="8262e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8262e-102">SYNOPSIS</span></span>
<span data-ttu-id="8262e-103">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8262e-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="8262e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8262e-104">SYNTAX</span></span>

### <span data-ttu-id="8262e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8262e-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8262e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8262e-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8262e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8262e-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="8262e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8262e-108">DESCRIPTION</span></span>
<span data-ttu-id="8262e-109">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8262e-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="8262e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8262e-110">EXAMPLES</span></span>

### <span data-ttu-id="8262e-111">Przykład 1. Lista wszystkich reguł sieci wirtualnej w określonym serwerze PostgreSql</span><span class="sxs-lookup"><span data-stu-id="8262e-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="8262e-112">To polecenie cmdlet wyświetla listę wszystkich reguł sieci wirtualnej na określonym serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="8262e-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="8262e-113">Przykład 2. Uzyskiwanie reguły wirtualnej sieci według nazwy</span><span class="sxs-lookup"><span data-stu-id="8262e-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="8262e-114">To polecenie cmdlet pobiera regułę wirtualnej sieci według nazwy.</span><span class="sxs-lookup"><span data-stu-id="8262e-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="8262e-115">Przykład 3. Uzyskiwanie reguły sieci wirtualnej za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="8262e-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="8262e-116">To polecenie cmdlet pobiera regułę wirtualnej sieci za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="8262e-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="8262e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8262e-117">PARAMETERS</span></span>

### <span data-ttu-id="8262e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8262e-118">-DefaultProfile</span></span>
<span data-ttu-id="8262e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8262e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8262e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8262e-120">-InputObject</span></span>
<span data-ttu-id="8262e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8262e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8262e-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8262e-122">-Name</span></span>
<span data-ttu-id="8262e-123">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8262e-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8262e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8262e-124">-PassThru</span></span>
<span data-ttu-id="8262e-125">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="8262e-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8262e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8262e-126">-ResourceGroupName</span></span>
<span data-ttu-id="8262e-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8262e-127">The name of the resource group.</span></span>
<span data-ttu-id="8262e-128">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="8262e-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8262e-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8262e-129">-ServerName</span></span>
<span data-ttu-id="8262e-130">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8262e-130">The name of the server.</span></span>

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

### <span data-ttu-id="8262e-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8262e-131">-SubscriptionId</span></span>
<span data-ttu-id="8262e-132">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8262e-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8262e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8262e-133">CommonParameters</span></span>
<span data-ttu-id="8262e-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8262e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8262e-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8262e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8262e-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8262e-136">INPUTS</span></span>

### <span data-ttu-id="8262e-137">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8262e-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="8262e-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8262e-138">OUTPUTS</span></span>

### <span data-ttu-id="8262e-139">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8262e-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="8262e-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8262e-140">NOTES</span></span>

<span data-ttu-id="8262e-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8262e-141">ALIASES</span></span>

<span data-ttu-id="8262e-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8262e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8262e-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8262e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8262e-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8262e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8262e-145">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="8262e-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8262e-146">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="8262e-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8262e-147">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8262e-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8262e-148">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8262e-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8262e-149">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8262e-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8262e-150">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8262e-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8262e-151">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8262e-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8262e-152">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="8262e-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="8262e-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="8262e-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8262e-154">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8262e-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8262e-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8262e-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8262e-156">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8262e-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8262e-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8262e-157">RELATED LINKS</span></span>

