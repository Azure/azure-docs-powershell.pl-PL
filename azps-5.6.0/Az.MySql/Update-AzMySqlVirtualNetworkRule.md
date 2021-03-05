---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 572943ea0f694b5a3a68ff4c1c030a1a3a1fc0f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968737"
---
# <span data-ttu-id="cb195-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cb195-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="cb195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb195-102">SYNOPSIS</span></span>
<span data-ttu-id="cb195-103">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cb195-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="cb195-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cb195-104">SYNTAX</span></span>

### <span data-ttu-id="cb195-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="cb195-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb195-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cb195-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb195-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cb195-107">DESCRIPTION</span></span>
<span data-ttu-id="cb195-108">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cb195-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="cb195-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cb195-109">EXAMPLES</span></span>

### <span data-ttu-id="cb195-110">Przykład 1. Aktualizowanie reguły wirtualnej sieci MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="cb195-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="cb195-111">To polecenie cmdlet aktualizuje wirtualną regułę sieci mysql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="cb195-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="cb195-112">Przykład 2. Aktualizowanie reguły sieci wirtualnej MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="cb195-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="cb195-113">Te polecenia cmdlet aktualizują wirtualną regułę sieci MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="cb195-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="cb195-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb195-114">PARAMETERS</span></span>

### <span data-ttu-id="cb195-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cb195-115">-AsJob</span></span>
<span data-ttu-id="cb195-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="cb195-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cb195-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb195-117">-DefaultProfile</span></span>
<span data-ttu-id="cb195-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb195-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb195-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb195-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="cb195-120">Utwórz regułę zapory, zanim sieć wirtualna będzie włączona dla punktu końcowego usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="cb195-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="cb195-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb195-121">-InputObject</span></span>
<span data-ttu-id="cb195-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cb195-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb195-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cb195-123">-Name</span></span>
<span data-ttu-id="cb195-124">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cb195-124">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb195-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cb195-125">-NoWait</span></span>
<span data-ttu-id="cb195-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="cb195-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cb195-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb195-127">-PassThru</span></span>
<span data-ttu-id="cb195-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="cb195-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cb195-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb195-129">-ResourceGroupName</span></span>
<span data-ttu-id="cb195-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb195-130">The name of the resource group.</span></span>
<span data-ttu-id="cb195-131">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="cb195-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb195-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb195-132">-ServerName</span></span>
<span data-ttu-id="cb195-133">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="cb195-133">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb195-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cb195-134">-SubnetId</span></span>
<span data-ttu-id="cb195-135">Identyfikator ARM sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cb195-135">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb195-136">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb195-136">-SubscriptionId</span></span>
<span data-ttu-id="cb195-137">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="cb195-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb195-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb195-138">-Confirm</span></span>
<span data-ttu-id="cb195-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cb195-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb195-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb195-140">-WhatIf</span></span>
<span data-ttu-id="cb195-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb195-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb195-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cb195-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb195-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb195-143">CommonParameters</span></span>
<span data-ttu-id="cb195-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb195-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb195-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb195-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb195-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb195-146">INPUTS</span></span>

### <span data-ttu-id="cb195-147">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cb195-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="cb195-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb195-148">OUTPUTS</span></span>

### <span data-ttu-id="cb195-149">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cb195-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="cb195-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cb195-150">NOTES</span></span>

<span data-ttu-id="cb195-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="cb195-151">ALIASES</span></span>

<span data-ttu-id="cb195-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb195-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb195-153">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cb195-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb195-154">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb195-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb195-155">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="cb195-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb195-156">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="cb195-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cb195-157">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="cb195-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cb195-158">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="cb195-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cb195-159">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cb195-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb195-160">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="cb195-160">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="cb195-161">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cb195-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cb195-162">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb195-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cb195-163">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="cb195-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="cb195-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="cb195-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cb195-165">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="cb195-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cb195-166">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="cb195-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cb195-167">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cb195-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cb195-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb195-168">RELATED LINKS</span></span>

