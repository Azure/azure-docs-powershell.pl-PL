---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234559"
---
# <span data-ttu-id="4fb9b-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4fb9b-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="4fb9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fb9b-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb9b-103">Umożliwia utworzenie lub zaktualizowanie istniejącej reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="4fb9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fb9b-104">SYNTAX</span></span>

### <span data-ttu-id="4fb9b-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4fb9b-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4fb9b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4fb9b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4fb9b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4fb9b-107">DESCRIPTION</span></span>
<span data-ttu-id="4fb9b-108">Umożliwia utworzenie lub zaktualizowanie istniejącej reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="4fb9b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fb9b-109">EXAMPLES</span></span>

### <span data-ttu-id="4fb9b-110">Przykład 1: reguła sieci wirtualnej aktualizacji MariaDB</span><span class="sxs-lookup"><span data-stu-id="4fb9b-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="4fb9b-111">To polecenie aktualizuje regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="4fb9b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fb9b-112">PARAMETERS</span></span>

### <span data-ttu-id="4fb9b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fb9b-113">-AsJob</span></span>
<span data-ttu-id="4fb9b-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4fb9b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4fb9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb9b-115">-DefaultProfile</span></span>
<span data-ttu-id="4fb9b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fb9b-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fb9b-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="4fb9b-118">Tworzenie reguły zapory przed włączeniem punktu końcowego usługi VNET w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="4fb9b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4fb9b-119">-InputObject</span></span>
<span data-ttu-id="4fb9b-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4fb9b-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4fb9b-121">-Name</span></span>
<span data-ttu-id="4fb9b-122">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="4fb9b-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4fb9b-123">-NoWait</span></span>
<span data-ttu-id="4fb9b-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4fb9b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4fb9b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fb9b-125">-PassThru</span></span>
<span data-ttu-id="4fb9b-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4fb9b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb9b-127">-ResourceGroupName</span></span>
<span data-ttu-id="4fb9b-128">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4fb9b-129">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4fb9b-130">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4fb9b-130">-ServerName</span></span>
<span data-ttu-id="4fb9b-131">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-131">The name of the server.</span></span>

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

### <span data-ttu-id="4fb9b-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4fb9b-132">-SubnetId</span></span>
<span data-ttu-id="4fb9b-133">Identyfikator zasobu ARM podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="4fb9b-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4fb9b-134">-SubscriptionId</span></span>
<span data-ttu-id="4fb9b-135">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="4fb9b-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4fb9b-136">-Confirm</span></span>
<span data-ttu-id="4fb9b-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fb9b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fb9b-138">-WhatIf</span></span>
<span data-ttu-id="4fb9b-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fb9b-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fb9b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb9b-141">CommonParameters</span></span>
<span data-ttu-id="4fb9b-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb9b-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fb9b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb9b-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fb9b-144">INPUTS</span></span>

### <span data-ttu-id="4fb9b-145">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="4fb9b-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="4fb9b-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fb9b-146">OUTPUTS</span></span>

### <span data-ttu-id="4fb9b-147">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4fb9b-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="4fb9b-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fb9b-148">NOTES</span></span>

<span data-ttu-id="4fb9b-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4fb9b-149">ALIASES</span></span>

<span data-ttu-id="4fb9b-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fb9b-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4fb9b-151">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4fb9b-152">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4fb9b-153">INPUTobject <IMariaDbIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4fb9b-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4fb9b-154">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4fb9b-155">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4fb9b-156">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4fb9b-157">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4fb9b-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4fb9b-158">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4fb9b-159">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4fb9b-160">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4fb9b-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4fb9b-162">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4fb9b-163">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="4fb9b-164">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4fb9b-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4fb9b-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fb9b-165">RELATED LINKS</span></span>

