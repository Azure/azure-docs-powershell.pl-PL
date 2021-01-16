---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 8756626488dcc1f5f2a41a06d30581a67db74bb3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349153"
---
# <span data-ttu-id="40768-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="40768-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="40768-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40768-102">SYNOPSIS</span></span>
<span data-ttu-id="40768-103">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="40768-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="40768-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40768-104">SYNTAX</span></span>

### <span data-ttu-id="40768-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="40768-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="40768-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="40768-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="40768-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="40768-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="40768-108">Opis</span><span class="sxs-lookup"><span data-stu-id="40768-108">DESCRIPTION</span></span>
<span data-ttu-id="40768-109">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="40768-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="40768-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40768-110">EXAMPLES</span></span>

### <span data-ttu-id="40768-111">Przykład 1: zawiera listę wszystkich reguł sieci wirtualnej określonych w serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="40768-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="40768-112">To polecenie cmdlet wyświetla listę wszystkich reguł sieci wirtualnej określonych na serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="40768-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="40768-113">Przykład 2: pobieranie reguły sieci wirtualnej według nazwy</span><span class="sxs-lookup"><span data-stu-id="40768-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="40768-114">To polecenie cmdlet pobiera regułę sieci wirtualnej według nazwy.</span><span class="sxs-lookup"><span data-stu-id="40768-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="40768-115">Przykład 3: pobieranie reguły sieci wirtualnej według tożsamości</span><span class="sxs-lookup"><span data-stu-id="40768-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="40768-116">To polecenie cmdlet pobiera regułę sieci wirtualnej według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="40768-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="40768-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40768-117">PARAMETERS</span></span>

### <span data-ttu-id="40768-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40768-118">-DefaultProfile</span></span>
<span data-ttu-id="40768-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40768-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40768-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="40768-120">-InputObject</span></span>
<span data-ttu-id="40768-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="40768-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="40768-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40768-122">-Name</span></span>
<span data-ttu-id="40768-123">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="40768-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="40768-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40768-124">-PassThru</span></span>
<span data-ttu-id="40768-125">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="40768-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="40768-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40768-126">-ResourceGroupName</span></span>
<span data-ttu-id="40768-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="40768-127">The name of the resource group.</span></span>
<span data-ttu-id="40768-128">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="40768-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="40768-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="40768-129">-ServerName</span></span>
<span data-ttu-id="40768-130">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="40768-130">The name of the server.</span></span>

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

### <span data-ttu-id="40768-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="40768-131">-SubscriptionId</span></span>
<span data-ttu-id="40768-132">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="40768-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="40768-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40768-133">CommonParameters</span></span>
<span data-ttu-id="40768-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40768-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40768-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40768-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40768-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40768-136">INPUTS</span></span>

### <span data-ttu-id="40768-137">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="40768-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="40768-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40768-138">OUTPUTS</span></span>

### <span data-ttu-id="40768-139">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="40768-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="40768-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40768-140">NOTES</span></span>

<span data-ttu-id="40768-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="40768-141">ALIASES</span></span>

<span data-ttu-id="40768-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40768-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40768-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="40768-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40768-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40768-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40768-145">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="40768-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40768-146">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="40768-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="40768-147">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="40768-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="40768-148">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="40768-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="40768-149">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="40768-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40768-150">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="40768-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="40768-151">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="40768-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="40768-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="40768-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="40768-153">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="40768-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="40768-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="40768-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="40768-155">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="40768-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="40768-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="40768-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="40768-157">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="40768-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="40768-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40768-158">RELATED LINKS</span></span>

