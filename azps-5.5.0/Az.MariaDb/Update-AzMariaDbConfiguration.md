---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192242"
---
# <span data-ttu-id="93a6d-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a6d-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="93a6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="93a6d-103">Aktualizuje konfigurację serwera.</span><span class="sxs-lookup"><span data-stu-id="93a6d-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="93a6d-104">Użyj Update-AzMariaDbServer, jeśli chcesz zaktualizować hasło AdministratorLoginPassword, sku itp.</span><span class="sxs-lookup"><span data-stu-id="93a6d-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="93a6d-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93a6d-105">SYNTAX</span></span>

### <span data-ttu-id="93a6d-106">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="93a6d-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="93a6d-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="93a6d-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93a6d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="93a6d-108">DESCRIPTION</span></span>
<span data-ttu-id="93a6d-109">Aktualizuje konfigurację serwera.</span><span class="sxs-lookup"><span data-stu-id="93a6d-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="93a6d-110">Użyj Update-AzMariaDberver, jeśli chcesz zaktualizować hasło AdministratorLoginPassword, sku itp.</span><span class="sxs-lookup"><span data-stu-id="93a6d-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="93a6d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93a6d-111">EXAMPLES</span></span>

### <span data-ttu-id="93a6d-112">Przykład 1. Aktualizowanie konfiguracji bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="93a6d-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="93a6d-113">To polecenie aktualizuje konfigurację bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="93a6d-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="93a6d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93a6d-114">PARAMETERS</span></span>

### <span data-ttu-id="93a6d-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="93a6d-115">-AsJob</span></span>
<span data-ttu-id="93a6d-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="93a6d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="93a6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a6d-117">-DefaultProfile</span></span>
<span data-ttu-id="93a6d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="93a6d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93a6d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93a6d-119">-InputObject</span></span>
<span data-ttu-id="93a6d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="93a6d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="93a6d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="93a6d-121">-Name</span></span>
<span data-ttu-id="93a6d-122">Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="93a6d-122">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a6d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="93a6d-123">-NoWait</span></span>
<span data-ttu-id="93a6d-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="93a6d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="93a6d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a6d-125">-ResourceGroupName</span></span>
<span data-ttu-id="93a6d-126">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="93a6d-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="93a6d-127">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="93a6d-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="93a6d-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93a6d-128">-ServerName</span></span>
<span data-ttu-id="93a6d-129">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="93a6d-129">The name of the server.</span></span>

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

### <span data-ttu-id="93a6d-130">— Źródło</span><span class="sxs-lookup"><span data-stu-id="93a6d-130">-Source</span></span>
<span data-ttu-id="93a6d-131">Źródło konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="93a6d-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="93a6d-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93a6d-132">-SubscriptionId</span></span>
<span data-ttu-id="93a6d-133">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="93a6d-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="93a6d-134">— Wartość</span><span class="sxs-lookup"><span data-stu-id="93a6d-134">-Value</span></span>
<span data-ttu-id="93a6d-135">Wartość konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="93a6d-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="93a6d-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93a6d-136">-Confirm</span></span>
<span data-ttu-id="93a6d-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="93a6d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93a6d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93a6d-138">-WhatIf</span></span>
<span data-ttu-id="93a6d-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93a6d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93a6d-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="93a6d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93a6d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a6d-141">CommonParameters</span></span>
<span data-ttu-id="93a6d-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93a6d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a6d-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93a6d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a6d-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93a6d-144">INPUTS</span></span>

### <span data-ttu-id="93a6d-145">Microsoft.Azure.PowerShell.Cmdlet.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="93a6d-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="93a6d-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93a6d-146">OUTPUTS</span></span>

### <span data-ttu-id="93a6d-147">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a6d-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="93a6d-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93a6d-148">NOTES</span></span>

<span data-ttu-id="93a6d-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="93a6d-149">ALIASES</span></span>

<span data-ttu-id="93a6d-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93a6d-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93a6d-151">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="93a6d-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93a6d-152">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93a6d-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93a6d-153">INPUTOBJECT: <IMariaDbIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="93a6d-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93a6d-154">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="93a6d-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="93a6d-155">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="93a6d-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="93a6d-156">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="93a6d-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="93a6d-157">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="93a6d-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93a6d-158">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="93a6d-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="93a6d-159">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="93a6d-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="93a6d-160">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="93a6d-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="93a6d-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="93a6d-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="93a6d-162">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="93a6d-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="93a6d-163">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="93a6d-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="93a6d-164">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="93a6d-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="93a6d-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93a6d-165">RELATED LINKS</span></span>

