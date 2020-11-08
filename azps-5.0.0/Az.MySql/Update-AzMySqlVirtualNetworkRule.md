---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: f98c24ab0be3b2c35ac43642fb9d4bbf0b421c7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225540"
---
# <span data-ttu-id="f111f-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f111f-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="f111f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f111f-102">SYNOPSIS</span></span>
<span data-ttu-id="f111f-103">Umożliwia utworzenie lub zaktualizowanie istniejącej reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f111f-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f111f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f111f-104">SYNTAX</span></span>

### <span data-ttu-id="f111f-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f111f-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f111f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f111f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f111f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f111f-107">DESCRIPTION</span></span>
<span data-ttu-id="f111f-108">Umożliwia utworzenie lub zaktualizowanie istniejącej reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f111f-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f111f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f111f-109">EXAMPLES</span></span>

### <span data-ttu-id="f111f-110">Przykład 1: Aktualizacja reguły sieci wirtualnej MySql według nazwy</span><span class="sxs-lookup"><span data-stu-id="f111f-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="f111f-111">To polecenie cmdlet powoduje zaktualizowanie reguły sieci wirtualnej MySql według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f111f-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="f111f-112">Przykład 2: aktualizowanie reguły sieci wirtualnej MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f111f-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="f111f-113">Te polecenia cmdlet aktualizują regułę sieci wirtualnej MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f111f-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="f111f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f111f-114">PARAMETERS</span></span>

### <span data-ttu-id="f111f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f111f-115">-AsJob</span></span>
<span data-ttu-id="f111f-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f111f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f111f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f111f-117">-DefaultProfile</span></span>
<span data-ttu-id="f111f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f111f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f111f-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f111f-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="f111f-120">Tworzenie reguły zapory przed włączeniem punktu końcowego usługi VNET w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f111f-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="f111f-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f111f-121">-InputObject</span></span>
<span data-ttu-id="f111f-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f111f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f111f-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f111f-123">-Name</span></span>
<span data-ttu-id="f111f-124">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f111f-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="f111f-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f111f-125">-NoWait</span></span>
<span data-ttu-id="f111f-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f111f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f111f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f111f-127">-PassThru</span></span>
<span data-ttu-id="f111f-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="f111f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f111f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f111f-129">-ResourceGroupName</span></span>
<span data-ttu-id="f111f-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f111f-130">The name of the resource group.</span></span>
<span data-ttu-id="f111f-131">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f111f-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f111f-132">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f111f-132">-ServerName</span></span>
<span data-ttu-id="f111f-133">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f111f-133">The name of the server.</span></span>

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

### <span data-ttu-id="f111f-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f111f-134">-SubnetId</span></span>
<span data-ttu-id="f111f-135">Identyfikator zasobu ARM podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f111f-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="f111f-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f111f-136">-SubscriptionId</span></span>
<span data-ttu-id="f111f-137">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f111f-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f111f-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f111f-138">-Confirm</span></span>
<span data-ttu-id="f111f-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f111f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f111f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f111f-140">-WhatIf</span></span>
<span data-ttu-id="f111f-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f111f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f111f-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f111f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f111f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f111f-143">CommonParameters</span></span>
<span data-ttu-id="f111f-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f111f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f111f-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f111f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f111f-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f111f-146">INPUTS</span></span>

### <span data-ttu-id="f111f-147">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f111f-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f111f-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f111f-148">OUTPUTS</span></span>

### <span data-ttu-id="f111f-149">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f111f-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="f111f-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f111f-150">NOTES</span></span>

<span data-ttu-id="f111f-151">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f111f-151">ALIASES</span></span>

<span data-ttu-id="f111f-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f111f-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f111f-153">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f111f-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f111f-154">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f111f-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f111f-155">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f111f-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f111f-156">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="f111f-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f111f-157">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f111f-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f111f-158">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f111f-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f111f-159">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f111f-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f111f-160">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f111f-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f111f-161">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f111f-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f111f-162">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f111f-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="f111f-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f111f-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f111f-164">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f111f-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f111f-165">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f111f-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f111f-166">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f111f-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f111f-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f111f-167">RELATED LINKS</span></span>

