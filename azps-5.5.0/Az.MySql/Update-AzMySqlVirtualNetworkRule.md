---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 7779a5405f50fe87f7a9e631b40cbdc8cb40fe5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180026"
---
# <span data-ttu-id="bd89c-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bd89c-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="bd89c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd89c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd89c-103">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bd89c-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="bd89c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bd89c-104">SYNTAX</span></span>

### <span data-ttu-id="bd89c-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="bd89c-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bd89c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bd89c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd89c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bd89c-107">DESCRIPTION</span></span>
<span data-ttu-id="bd89c-108">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bd89c-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="bd89c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bd89c-109">EXAMPLES</span></span>

### <span data-ttu-id="bd89c-110">Przykład 1. Aktualizowanie reguły wirtualnej sieci MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="bd89c-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="bd89c-111">To polecenie cmdlet aktualizuje wirtualną regułę sieci mysql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="bd89c-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="bd89c-112">Przykład 2. Aktualizowanie reguły sieci wirtualnej MySql przez tożsamość.</span><span class="sxs-lookup"><span data-stu-id="bd89c-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="bd89c-113">Te polecenia cmdlet aktualizują wirtualną regułę sieci MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bd89c-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="bd89c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd89c-114">PARAMETERS</span></span>

### <span data-ttu-id="bd89c-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bd89c-115">-AsJob</span></span>
<span data-ttu-id="bd89c-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="bd89c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bd89c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd89c-117">-DefaultProfile</span></span>
<span data-ttu-id="bd89c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd89c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd89c-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd89c-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="bd89c-120">Utwórz regułę zapory, zanim sieć wirtualna będzie włączona dla punktu końcowego usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="bd89c-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="bd89c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd89c-121">-InputObject</span></span>
<span data-ttu-id="bd89c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bd89c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bd89c-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bd89c-123">-Name</span></span>
<span data-ttu-id="bd89c-124">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bd89c-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="bd89c-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bd89c-125">-NoWait</span></span>
<span data-ttu-id="bd89c-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="bd89c-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bd89c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd89c-127">-PassThru</span></span>
<span data-ttu-id="bd89c-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="bd89c-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bd89c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd89c-129">-ResourceGroupName</span></span>
<span data-ttu-id="bd89c-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd89c-130">The name of the resource group.</span></span>
<span data-ttu-id="bd89c-131">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="bd89c-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bd89c-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bd89c-132">-ServerName</span></span>
<span data-ttu-id="bd89c-133">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bd89c-133">The name of the server.</span></span>

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

### <span data-ttu-id="bd89c-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bd89c-134">-SubnetId</span></span>
<span data-ttu-id="bd89c-135">Identyfikator ARM sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bd89c-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="bd89c-136">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd89c-136">-SubscriptionId</span></span>
<span data-ttu-id="bd89c-137">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="bd89c-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bd89c-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd89c-138">-Confirm</span></span>
<span data-ttu-id="bd89c-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bd89c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd89c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd89c-140">-WhatIf</span></span>
<span data-ttu-id="bd89c-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd89c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd89c-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bd89c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd89c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd89c-143">CommonParameters</span></span>
<span data-ttu-id="bd89c-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd89c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd89c-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd89c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd89c-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd89c-146">INPUTS</span></span>

### <span data-ttu-id="bd89c-147">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bd89c-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bd89c-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd89c-148">OUTPUTS</span></span>

### <span data-ttu-id="bd89c-149">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bd89c-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="bd89c-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bd89c-150">NOTES</span></span>

<span data-ttu-id="bd89c-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="bd89c-151">ALIASES</span></span>

<span data-ttu-id="bd89c-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd89c-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd89c-153">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bd89c-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd89c-154">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bd89c-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd89c-155">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="bd89c-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bd89c-156">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="bd89c-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bd89c-157">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bd89c-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bd89c-158">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="bd89c-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bd89c-159">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bd89c-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bd89c-160">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="bd89c-160">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="bd89c-161">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="bd89c-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bd89c-162">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd89c-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bd89c-163">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="bd89c-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="bd89c-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="bd89c-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bd89c-165">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bd89c-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bd89c-166">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="bd89c-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bd89c-167">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bd89c-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bd89c-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd89c-168">RELATED LINKS</span></span>

