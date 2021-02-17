---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183971"
---
# <span data-ttu-id="b186f-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b186f-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="b186f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b186f-102">SYNOPSIS</span></span>
<span data-ttu-id="b186f-103">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b186f-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="b186f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b186f-104">SYNTAX</span></span>

### <span data-ttu-id="b186f-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="b186f-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b186f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b186f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b186f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b186f-107">DESCRIPTION</span></span>
<span data-ttu-id="b186f-108">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b186f-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="b186f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b186f-109">EXAMPLES</span></span>

### <span data-ttu-id="b186f-110">Przykład 1. Aktualizowanie reguły wirtualnej sieci postgresql według nazwy</span><span class="sxs-lookup"><span data-stu-id="b186f-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="b186f-111">To polecenie cmdlet aktualizuje regułę PostgreSql Virtual Network Rule według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b186f-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="b186f-112">Przykład 2. Aktualizowanie reguły sieci wirtualnej PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="b186f-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="b186f-113">Te polecenia cmdlet aktualizują regułę postgresql wirtualnej sieci według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="b186f-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="b186f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b186f-114">PARAMETERS</span></span>

### <span data-ttu-id="b186f-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b186f-115">-AsJob</span></span>
<span data-ttu-id="b186f-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b186f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b186f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b186f-117">-DefaultProfile</span></span>
<span data-ttu-id="b186f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b186f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b186f-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b186f-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b186f-120">Utwórz regułę zapory, zanim sieć wirtualna będzie włączona dla punktu końcowego usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="b186f-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b186f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b186f-121">-InputObject</span></span>
<span data-ttu-id="b186f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b186f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b186f-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b186f-123">-Name</span></span>
<span data-ttu-id="b186f-124">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b186f-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b186f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b186f-125">-NoWait</span></span>
<span data-ttu-id="b186f-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b186f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b186f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b186f-127">-PassThru</span></span>
<span data-ttu-id="b186f-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="b186f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b186f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b186f-129">-ResourceGroupName</span></span>
<span data-ttu-id="b186f-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b186f-130">The name of the resource group.</span></span>
<span data-ttu-id="b186f-131">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b186f-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b186f-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b186f-132">-ServerName</span></span>
<span data-ttu-id="b186f-133">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b186f-133">The name of the server.</span></span>

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

### <span data-ttu-id="b186f-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b186f-134">-SubnetId</span></span>
<span data-ttu-id="b186f-135">Identyfikator ARM sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b186f-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="b186f-136">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b186f-136">-SubscriptionId</span></span>
<span data-ttu-id="b186f-137">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b186f-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b186f-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b186f-138">-Confirm</span></span>
<span data-ttu-id="b186f-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b186f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b186f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b186f-140">-WhatIf</span></span>
<span data-ttu-id="b186f-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b186f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b186f-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b186f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b186f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b186f-143">CommonParameters</span></span>
<span data-ttu-id="b186f-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b186f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b186f-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b186f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b186f-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b186f-146">INPUTS</span></span>

### <span data-ttu-id="b186f-147">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b186f-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b186f-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b186f-148">OUTPUTS</span></span>

### <span data-ttu-id="b186f-149">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b186f-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="b186f-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b186f-150">NOTES</span></span>

<span data-ttu-id="b186f-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b186f-151">ALIASES</span></span>

<span data-ttu-id="b186f-152">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b186f-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b186f-153">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b186f-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b186f-154">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b186f-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b186f-155">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b186f-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b186f-156">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="b186f-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b186f-157">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b186f-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b186f-158">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="b186f-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b186f-159">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b186f-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b186f-160">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b186f-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b186f-161">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b186f-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b186f-162">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b186f-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="b186f-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="b186f-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b186f-164">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b186f-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b186f-165">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b186f-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b186f-166">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b186f-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b186f-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b186f-167">RELATED LINKS</span></span>

