---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: e5eb6e239ef49dccf610be866a0f9711245d5ba5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986714"
---
# <span data-ttu-id="fc327-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fc327-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="fc327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc327-102">SYNOPSIS</span></span>
<span data-ttu-id="fc327-103">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fc327-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="fc327-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fc327-104">SYNTAX</span></span>

### <span data-ttu-id="fc327-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fc327-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="fc327-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="fc327-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="fc327-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fc327-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="fc327-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fc327-108">DESCRIPTION</span></span>
<span data-ttu-id="fc327-109">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fc327-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="fc327-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fc327-110">EXAMPLES</span></span>

### <span data-ttu-id="fc327-111">Przykład 1. Lista wszystkich reguł sieci wirtualnej w określonym serwerze PostgreSql</span><span class="sxs-lookup"><span data-stu-id="fc327-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="fc327-112">To polecenie cmdlet wyświetla listę wszystkich reguł sieci wirtualnej na określonym serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="fc327-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="fc327-113">Przykład 2. Uzyskiwanie reguły wirtualnej sieci według nazwy</span><span class="sxs-lookup"><span data-stu-id="fc327-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="fc327-114">To polecenie cmdlet otrzymuje regułę wirtualnej sieci według nazwy.</span><span class="sxs-lookup"><span data-stu-id="fc327-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="fc327-115">Przykład 3. Uzyskiwanie reguły sieci wirtualnej za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="fc327-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="fc327-116">To polecenie cmdlet pobiera regułę sieci wirtualnej za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="fc327-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="fc327-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc327-117">PARAMETERS</span></span>

### <span data-ttu-id="fc327-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc327-118">-DefaultProfile</span></span>
<span data-ttu-id="fc327-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc327-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc327-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc327-120">-InputObject</span></span>
<span data-ttu-id="fc327-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fc327-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fc327-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fc327-122">-Name</span></span>
<span data-ttu-id="fc327-123">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fc327-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="fc327-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc327-124">-PassThru</span></span>
<span data-ttu-id="fc327-125">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="fc327-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fc327-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc327-126">-ResourceGroupName</span></span>
<span data-ttu-id="fc327-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc327-127">The name of the resource group.</span></span>
<span data-ttu-id="fc327-128">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="fc327-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fc327-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fc327-129">-ServerName</span></span>
<span data-ttu-id="fc327-130">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="fc327-130">The name of the server.</span></span>

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

### <span data-ttu-id="fc327-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc327-131">-SubscriptionId</span></span>
<span data-ttu-id="fc327-132">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="fc327-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fc327-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc327-133">CommonParameters</span></span>
<span data-ttu-id="fc327-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc327-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc327-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc327-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc327-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc327-136">INPUTS</span></span>

### <span data-ttu-id="fc327-137">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fc327-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="fc327-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc327-138">OUTPUTS</span></span>

### <span data-ttu-id="fc327-139">Microsoft.Azure.PowerShell.cmdlet.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fc327-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="fc327-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fc327-140">NOTES</span></span>

<span data-ttu-id="fc327-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fc327-141">ALIASES</span></span>

<span data-ttu-id="fc327-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc327-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fc327-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fc327-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc327-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fc327-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fc327-145">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="fc327-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fc327-146">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="fc327-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fc327-147">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fc327-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fc327-148">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="fc327-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fc327-149">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="fc327-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fc327-150">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="fc327-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fc327-151">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc327-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fc327-152">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="fc327-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="fc327-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="fc327-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fc327-154">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="fc327-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fc327-155">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="fc327-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fc327-156">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fc327-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fc327-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc327-157">RELATED LINKS</span></span>

