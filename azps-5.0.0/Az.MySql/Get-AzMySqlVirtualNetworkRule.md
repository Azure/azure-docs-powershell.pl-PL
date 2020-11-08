---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 91d774931ac7ef4b8f1d41a70953d4a5b3a322cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232160"
---
# <span data-ttu-id="73945-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="73945-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="73945-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73945-102">SYNOPSIS</span></span>
<span data-ttu-id="73945-103">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="73945-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="73945-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73945-104">SYNTAX</span></span>

### <span data-ttu-id="73945-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="73945-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="73945-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="73945-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="73945-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73945-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="73945-108">Opis</span><span class="sxs-lookup"><span data-stu-id="73945-108">DESCRIPTION</span></span>
<span data-ttu-id="73945-109">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="73945-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="73945-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73945-110">EXAMPLES</span></span>

### <span data-ttu-id="73945-111">Przykład 1: zawiera listę wszystkich reguł sieci wirtualnej określonych w serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="73945-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="73945-112">To polecenie cmdlet wyświetla listę wszystkich reguł sieci wirtualnej określonych na serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="73945-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="73945-113">Przykład 2: pobieranie reguły sieci wirtualnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="73945-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="73945-114">To polecenie cmdlet pobiera regułę sieci wirtualnej według nazwy.</span><span class="sxs-lookup"><span data-stu-id="73945-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="73945-115">Przykład 3: pobieranie reguły sieci wirtualnej według tożsamości</span><span class="sxs-lookup"><span data-stu-id="73945-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="73945-116">To polecenie cmdlet pobiera regułę sieci wirtualnej według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="73945-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="73945-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73945-117">PARAMETERS</span></span>

### <span data-ttu-id="73945-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73945-118">-DefaultProfile</span></span>
<span data-ttu-id="73945-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73945-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73945-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="73945-120">-InputObject</span></span>
<span data-ttu-id="73945-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="73945-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73945-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73945-122">-Name</span></span>
<span data-ttu-id="73945-123">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="73945-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="73945-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73945-124">-PassThru</span></span>
<span data-ttu-id="73945-125">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="73945-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="73945-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73945-126">-ResourceGroupName</span></span>
<span data-ttu-id="73945-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73945-127">The name of the resource group.</span></span>
<span data-ttu-id="73945-128">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="73945-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="73945-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="73945-129">-ServerName</span></span>
<span data-ttu-id="73945-130">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="73945-130">The name of the server.</span></span>

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

### <span data-ttu-id="73945-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="73945-131">-SubscriptionId</span></span>
<span data-ttu-id="73945-132">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="73945-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="73945-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73945-133">CommonParameters</span></span>
<span data-ttu-id="73945-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73945-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73945-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73945-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73945-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73945-136">INPUTS</span></span>

### <span data-ttu-id="73945-137">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="73945-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="73945-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73945-138">OUTPUTS</span></span>

### <span data-ttu-id="73945-139">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="73945-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="73945-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73945-140">NOTES</span></span>

<span data-ttu-id="73945-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="73945-141">ALIASES</span></span>

<span data-ttu-id="73945-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73945-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73945-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="73945-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73945-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73945-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73945-145">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="73945-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73945-146">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="73945-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="73945-147">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="73945-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="73945-148">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="73945-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="73945-149">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="73945-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73945-150">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="73945-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="73945-151">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73945-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="73945-152">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="73945-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="73945-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="73945-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="73945-154">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="73945-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="73945-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="73945-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="73945-156">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="73945-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="73945-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73945-157">RELATED LINKS</span></span>

