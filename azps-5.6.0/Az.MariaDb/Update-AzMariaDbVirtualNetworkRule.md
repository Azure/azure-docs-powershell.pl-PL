---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cbb774e0a4bedb66a32839c069c305317c8e9f43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003857"
---
# <span data-ttu-id="3d4af-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3d4af-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="3d4af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d4af-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4af-103">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3d4af-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="3d4af-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3d4af-104">SYNTAX</span></span>

### <span data-ttu-id="3d4af-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3d4af-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3d4af-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3d4af-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3d4af-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3d4af-107">DESCRIPTION</span></span>
<span data-ttu-id="3d4af-108">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3d4af-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="3d4af-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3d4af-109">EXAMPLES</span></span>

### <span data-ttu-id="3d4af-110">Przykład 1. Aktualizowanie reguły sieci wirtualnej MariaDB</span><span class="sxs-lookup"><span data-stu-id="3d4af-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="3d4af-111">To polecenie aktualizuje regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3d4af-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="3d4af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d4af-112">PARAMETERS</span></span>

### <span data-ttu-id="3d4af-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3d4af-113">-AsJob</span></span>
<span data-ttu-id="3d4af-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="3d4af-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3d4af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4af-115">-DefaultProfile</span></span>
<span data-ttu-id="3d4af-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d4af-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d4af-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="3d4af-118">Utwórz regułę zapory, zanim sieć wirtualna będzie włączona dla punktu końcowego usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="3d4af-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="3d4af-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d4af-119">-InputObject</span></span>
<span data-ttu-id="3d4af-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3d4af-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4af-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3d4af-121">-Name</span></span>
<span data-ttu-id="3d4af-122">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3d4af-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="3d4af-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3d4af-123">-NoWait</span></span>
<span data-ttu-id="3d4af-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="3d4af-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3d4af-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d4af-125">-PassThru</span></span>
<span data-ttu-id="3d4af-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="3d4af-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3d4af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d4af-127">-ResourceGroupName</span></span>
<span data-ttu-id="3d4af-128">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="3d4af-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3d4af-129">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="3d4af-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3d4af-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d4af-130">-ServerName</span></span>
<span data-ttu-id="3d4af-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="3d4af-131">The name of the server.</span></span>

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

### <span data-ttu-id="3d4af-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3d4af-132">-SubnetId</span></span>
<span data-ttu-id="3d4af-133">Identyfikator ARM sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3d4af-133">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4af-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d4af-134">-SubscriptionId</span></span>
<span data-ttu-id="3d4af-135">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4af-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3d4af-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d4af-136">-Confirm</span></span>
<span data-ttu-id="3d4af-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3d4af-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d4af-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d4af-138">-WhatIf</span></span>
<span data-ttu-id="3d4af-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d4af-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d4af-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3d4af-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d4af-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4af-141">CommonParameters</span></span>
<span data-ttu-id="3d4af-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d4af-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4af-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d4af-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4af-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d4af-144">INPUTS</span></span>

### <span data-ttu-id="3d4af-145">Microsoft.Azure.PowerShell.Cmdlet.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="3d4af-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="3d4af-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d4af-146">OUTPUTS</span></span>

### <span data-ttu-id="3d4af-147">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3d4af-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="3d4af-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3d4af-148">NOTES</span></span>

<span data-ttu-id="3d4af-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3d4af-149">ALIASES</span></span>

<span data-ttu-id="3d4af-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d4af-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d4af-151">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3d4af-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d4af-152">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d4af-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d4af-153">INPUTOBJECT: <IMariaDbIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="3d4af-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d4af-154">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="3d4af-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3d4af-155">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3d4af-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3d4af-156">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="3d4af-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3d4af-157">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3d4af-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d4af-158">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="3d4af-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3d4af-159">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="3d4af-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3d4af-160">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="3d4af-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3d4af-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3d4af-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3d4af-162">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="3d4af-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3d4af-163">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4af-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="3d4af-164">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3d4af-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3d4af-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d4af-165">RELATED LINKS</span></span>

