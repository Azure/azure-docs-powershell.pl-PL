---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378436"
---
# <span data-ttu-id="45098-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="45098-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="45098-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45098-102">SYNOPSIS</span></span>
<span data-ttu-id="45098-103">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45098-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="45098-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45098-104">SYNTAX</span></span>

### <span data-ttu-id="45098-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="45098-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="45098-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="45098-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="45098-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45098-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="45098-108">Opis</span><span class="sxs-lookup"><span data-stu-id="45098-108">DESCRIPTION</span></span>
<span data-ttu-id="45098-109">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45098-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="45098-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45098-110">EXAMPLES</span></span>

### <span data-ttu-id="45098-111">Przykład 1: zawiera listę wszystkich reguł sieci wirtualnej na określonym serwerze PostgreSql</span><span class="sxs-lookup"><span data-stu-id="45098-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="45098-112">To polecenie cmdlet wyświetla listę wszystkich reguł sieci wirtualnej określonych na serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="45098-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="45098-113">Przykład 2: pobieranie reguły sieci wirtualnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="45098-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="45098-114">To polecenie cmdlet pobiera regułę sieci wirtualnej według nazwy.</span><span class="sxs-lookup"><span data-stu-id="45098-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="45098-115">Przykład 3: pobieranie reguły sieci wirtualnej według tożsamości</span><span class="sxs-lookup"><span data-stu-id="45098-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="45098-116">To polecenie cmdlet pobiera regułę sieci wirtualnej według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="45098-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="45098-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45098-117">PARAMETERS</span></span>

### <span data-ttu-id="45098-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45098-118">-DefaultProfile</span></span>
<span data-ttu-id="45098-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45098-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45098-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="45098-120">-InputObject</span></span>
<span data-ttu-id="45098-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="45098-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="45098-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45098-122">-Name</span></span>
<span data-ttu-id="45098-123">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45098-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="45098-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45098-124">-PassThru</span></span>
<span data-ttu-id="45098-125">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="45098-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="45098-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45098-126">-ResourceGroupName</span></span>
<span data-ttu-id="45098-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45098-127">The name of the resource group.</span></span>
<span data-ttu-id="45098-128">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="45098-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="45098-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="45098-129">-ServerName</span></span>
<span data-ttu-id="45098-130">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="45098-130">The name of the server.</span></span>

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

### <span data-ttu-id="45098-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="45098-131">-SubscriptionId</span></span>
<span data-ttu-id="45098-132">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="45098-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="45098-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45098-133">CommonParameters</span></span>
<span data-ttu-id="45098-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45098-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45098-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45098-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45098-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45098-136">INPUTS</span></span>

### <span data-ttu-id="45098-137">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="45098-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="45098-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45098-138">OUTPUTS</span></span>

### <span data-ttu-id="45098-139">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="45098-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="45098-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45098-140">NOTES</span></span>

<span data-ttu-id="45098-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="45098-141">ALIASES</span></span>

<span data-ttu-id="45098-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45098-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45098-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="45098-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45098-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45098-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45098-145">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="45098-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45098-146">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="45098-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="45098-147">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="45098-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="45098-148">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="45098-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="45098-149">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="45098-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45098-150">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="45098-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="45098-151">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45098-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="45098-152">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="45098-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="45098-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="45098-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="45098-154">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="45098-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="45098-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="45098-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="45098-156">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45098-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="45098-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45098-157">RELATED LINKS</span></span>

