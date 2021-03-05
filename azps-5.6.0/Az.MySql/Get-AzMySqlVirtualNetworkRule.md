---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 30e361d77f3c3b738703e1dde075ccbabc38b0b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979850"
---
# <span data-ttu-id="9fa6a-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9fa6a-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="9fa6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fa6a-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa6a-103">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="9fa6a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9fa6a-104">SYNTAX</span></span>

### <span data-ttu-id="9fa6a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="9fa6a-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9fa6a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="9fa6a-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9fa6a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9fa6a-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="9fa6a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9fa6a-108">DESCRIPTION</span></span>
<span data-ttu-id="9fa6a-109">Pobiera regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="9fa6a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9fa6a-110">EXAMPLES</span></span>

### <span data-ttu-id="9fa6a-111">Przykład 1. Lista wszystkich reguł sieci wirtualnej w określonym serwerze MySql</span><span class="sxs-lookup"><span data-stu-id="9fa6a-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="9fa6a-112">To polecenie cmdlet wyświetla listę wszystkich reguł sieci wirtualnej na określonym serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="9fa6a-113">Przykład 2. Uzyskiwanie reguły wirtualnej sieci według nazwy</span><span class="sxs-lookup"><span data-stu-id="9fa6a-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="9fa6a-114">To polecenie cmdlet otrzymuje regułę wirtualnej sieci według nazwy.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="9fa6a-115">Przykład 3. Uzyskiwanie reguły sieci wirtualnej za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="9fa6a-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="9fa6a-116">To polecenie cmdlet pobiera regułę sieci wirtualnej za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="9fa6a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fa6a-117">PARAMETERS</span></span>

### <span data-ttu-id="9fa6a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa6a-118">-DefaultProfile</span></span>
<span data-ttu-id="9fa6a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fa6a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fa6a-120">-InputObject</span></span>
<span data-ttu-id="9fa6a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9fa6a-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9fa6a-122">-Name</span></span>
<span data-ttu-id="9fa6a-123">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="9fa6a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fa6a-124">-PassThru</span></span>
<span data-ttu-id="9fa6a-125">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9fa6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="9fa6a-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-127">The name of the resource group.</span></span>
<span data-ttu-id="9fa6a-128">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9fa6a-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9fa6a-129">-ServerName</span></span>
<span data-ttu-id="9fa6a-130">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-130">The name of the server.</span></span>

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

### <span data-ttu-id="9fa6a-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9fa6a-131">-SubscriptionId</span></span>
<span data-ttu-id="9fa6a-132">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9fa6a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa6a-133">CommonParameters</span></span>
<span data-ttu-id="9fa6a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa6a-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fa6a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa6a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fa6a-136">INPUTS</span></span>

### <span data-ttu-id="9fa6a-137">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9fa6a-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9fa6a-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fa6a-138">OUTPUTS</span></span>

### <span data-ttu-id="9fa6a-139">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9fa6a-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="9fa6a-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9fa6a-140">NOTES</span></span>

<span data-ttu-id="9fa6a-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9fa6a-141">ALIASES</span></span>

<span data-ttu-id="9fa6a-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fa6a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9fa6a-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9fa6a-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9fa6a-145">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="9fa6a-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9fa6a-146">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9fa6a-147">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9fa6a-148">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9fa6a-149">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9fa6a-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9fa6a-150">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="9fa6a-151">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9fa6a-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9fa6a-153">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="9fa6a-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9fa6a-155">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9fa6a-156">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9fa6a-157">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9fa6a-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fa6a-158">RELATED LINKS</span></span>

