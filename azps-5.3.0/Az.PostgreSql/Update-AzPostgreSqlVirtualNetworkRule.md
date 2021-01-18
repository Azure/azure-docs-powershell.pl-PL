---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500078"
---
# <span data-ttu-id="259d4-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="259d4-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="259d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="259d4-102">SYNOPSIS</span></span>
<span data-ttu-id="259d4-103">Umożliwia utworzenie lub zaktualizowanie istniejącej reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="259d4-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="259d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="259d4-104">SYNTAX</span></span>

### <span data-ttu-id="259d4-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="259d4-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="259d4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="259d4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="259d4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="259d4-107">DESCRIPTION</span></span>
<span data-ttu-id="259d4-108">Umożliwia utworzenie lub zaktualizowanie istniejącej reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="259d4-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="259d4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="259d4-109">EXAMPLES</span></span>

### <span data-ttu-id="259d4-110">Przykład 1: aktualizowanie reguły sieci wirtualnej PostgreSql według nazwy</span><span class="sxs-lookup"><span data-stu-id="259d4-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="259d4-111">To polecenie cmdlet aktualizuje PostgreSql sieci wirtualnej według nazwy.</span><span class="sxs-lookup"><span data-stu-id="259d4-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="259d4-112">Przykład 2: aktualizowanie reguły sieci wirtualnej PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="259d4-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="259d4-113">Te polecenia cmdlet aktualizują regułę sieci wirtualnej PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="259d4-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="259d4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="259d4-114">PARAMETERS</span></span>

### <span data-ttu-id="259d4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="259d4-115">-AsJob</span></span>
<span data-ttu-id="259d4-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="259d4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="259d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="259d4-117">-DefaultProfile</span></span>
<span data-ttu-id="259d4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="259d4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="259d4-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="259d4-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="259d4-120">Tworzenie reguły zapory przed włączeniem punktu końcowego usługi VNET w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="259d4-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="259d4-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="259d4-121">-InputObject</span></span>
<span data-ttu-id="259d4-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="259d4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="259d4-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="259d4-123">-Name</span></span>
<span data-ttu-id="259d4-124">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="259d4-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="259d4-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="259d4-125">-NoWait</span></span>
<span data-ttu-id="259d4-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="259d4-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="259d4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="259d4-127">-PassThru</span></span>
<span data-ttu-id="259d4-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="259d4-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="259d4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259d4-129">-ResourceGroupName</span></span>
<span data-ttu-id="259d4-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="259d4-130">The name of the resource group.</span></span>
<span data-ttu-id="259d4-131">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="259d4-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="259d4-132">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="259d4-132">-ServerName</span></span>
<span data-ttu-id="259d4-133">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="259d4-133">The name of the server.</span></span>

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

### <span data-ttu-id="259d4-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="259d4-134">-SubnetId</span></span>
<span data-ttu-id="259d4-135">Identyfikator zasobu ARM podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="259d4-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="259d4-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="259d4-136">-SubscriptionId</span></span>
<span data-ttu-id="259d4-137">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="259d4-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="259d4-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="259d4-138">-Confirm</span></span>
<span data-ttu-id="259d4-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="259d4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="259d4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="259d4-140">-WhatIf</span></span>
<span data-ttu-id="259d4-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="259d4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="259d4-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="259d4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="259d4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259d4-143">CommonParameters</span></span>
<span data-ttu-id="259d4-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="259d4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259d4-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="259d4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259d4-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="259d4-146">INPUTS</span></span>

### <span data-ttu-id="259d4-147">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="259d4-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="259d4-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="259d4-148">OUTPUTS</span></span>

### <span data-ttu-id="259d4-149">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="259d4-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="259d4-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="259d4-150">NOTES</span></span>

<span data-ttu-id="259d4-151">PISUJE</span><span class="sxs-lookup"><span data-stu-id="259d4-151">ALIASES</span></span>

<span data-ttu-id="259d4-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="259d4-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="259d4-153">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="259d4-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="259d4-154">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="259d4-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="259d4-155">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="259d4-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="259d4-156">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="259d4-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="259d4-157">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="259d4-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="259d4-158">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="259d4-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="259d4-159">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="259d4-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="259d4-160">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="259d4-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="259d4-161">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="259d4-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="259d4-162">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="259d4-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="259d4-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="259d4-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="259d4-164">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="259d4-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="259d4-165">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="259d4-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="259d4-166">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="259d4-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="259d4-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="259d4-167">RELATED LINKS</span></span>

