---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194147"
---
# <span data-ttu-id="0c34a-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="0c34a-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="0c34a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c34a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c34a-103">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="0c34a-103">Updates an existing server.</span></span>
<span data-ttu-id="0c34a-104">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="0c34a-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="0c34a-105">Użyj Update-AzMariaDbConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="0c34a-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="0c34a-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c34a-106">SYNTAX</span></span>

### <span data-ttu-id="0c34a-107">Nazwa_serwera (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0c34a-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0c34a-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="0c34a-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c34a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c34a-109">DESCRIPTION</span></span>
<span data-ttu-id="0c34a-110">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="0c34a-110">Updates an existing server.</span></span>
<span data-ttu-id="0c34a-111">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="0c34a-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="0c34a-112">Użyj Update-AzMariaDbConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="0c34a-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="0c34a-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c34a-113">EXAMPLES</span></span>

### <span data-ttu-id="0c34a-114">Przykład 1. Aktualizacja bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="0c34a-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="0c34a-115">To polecenie aktualizuje plik MariaDB.</span><span class="sxs-lookup"><span data-stu-id="0c34a-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="0c34a-116">Przykład 2. Aktualizacja bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="0c34a-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="0c34a-117">To polecenie aktualizuje plik MariaDB.</span><span class="sxs-lookup"><span data-stu-id="0c34a-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="0c34a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c34a-118">PARAMETERS</span></span>

### <span data-ttu-id="0c34a-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="0c34a-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="0c34a-120">Hasło logowania administratora.</span><span class="sxs-lookup"><span data-stu-id="0c34a-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0c34a-121">-AsJob</span></span>
<span data-ttu-id="0c34a-122">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0c34a-122">Run the command as a job</span></span>

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

### <span data-ttu-id="0c34a-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="0c34a-123">-BackupRetentionDay</span></span>
<span data-ttu-id="0c34a-124">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="0c34a-124">Backup retention days for the server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c34a-125">-DefaultProfile</span></span>
<span data-ttu-id="0c34a-126">Region DefaultParameters Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c34a-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c34a-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="0c34a-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="0c34a-128">Włączanie nadmiarowej lokalizacji geograficznej dla kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="0c34a-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c34a-129">-InputObject</span></span>
<span data-ttu-id="0c34a-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0c34a-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0c34a-131">-Name</span></span>
<span data-ttu-id="0c34a-132">Nazwa serwera MariaDB</span><span class="sxs-lookup"><span data-stu-id="0c34a-132">MariaDB server name</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0c34a-133">-NoWait</span></span>
<span data-ttu-id="0c34a-134">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0c34a-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0c34a-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="0c34a-135">-ReplicationRole</span></span>
<span data-ttu-id="0c34a-136">Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="0c34a-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="0c34a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c34a-137">-ResourceGroupName</span></span>
<span data-ttu-id="0c34a-138">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="0c34a-138">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-139">- SKU</span><span class="sxs-lookup"><span data-stu-id="0c34a-139">-Sku</span></span>
<span data-ttu-id="0c34a-140">Nazwa sKU, zwykle warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0c34a-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="0c34a-141">- SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="0c34a-141">-SslEnforcement</span></span>
<span data-ttu-id="0c34a-142">Włączanie wymuszania ssl lub nie w przypadku nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="0c34a-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-143">- StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="0c34a-143">-StorageAutogrow</span></span>
<span data-ttu-id="0c34a-144">Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="0c34a-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-145">- StorageInMb</span><span class="sxs-lookup"><span data-stu-id="0c34a-145">-StorageInMb</span></span>
<span data-ttu-id="0c34a-146">Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="0c34a-146">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-147">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c34a-147">-SubscriptionId</span></span>
<span data-ttu-id="0c34a-148">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi</span><span class="sxs-lookup"><span data-stu-id="0c34a-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-149">— Tag</span><span class="sxs-lookup"><span data-stu-id="0c34a-149">-Tag</span></span>
<span data-ttu-id="0c34a-150">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="0c34a-150">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34a-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c34a-151">-Confirm</span></span>
<span data-ttu-id="0c34a-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c34a-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c34a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c34a-153">-WhatIf</span></span>
<span data-ttu-id="0c34a-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c34a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c34a-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0c34a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c34a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c34a-156">CommonParameters</span></span>
<span data-ttu-id="0c34a-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c34a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c34a-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c34a-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c34a-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c34a-159">INPUTS</span></span>

### <span data-ttu-id="0c34a-160">Microsoft.Azure.PowerShell.Cmdlet.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="0c34a-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="0c34a-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c34a-161">OUTPUTS</span></span>

### <span data-ttu-id="0c34a-162">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="0c34a-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0c34a-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c34a-163">NOTES</span></span>

<span data-ttu-id="0c34a-164">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0c34a-164">ALIASES</span></span>

<span data-ttu-id="0c34a-165">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0c34a-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0c34a-166">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0c34a-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0c34a-167">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0c34a-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0c34a-168">INPUTOBJECT: <IMariaDbIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="0c34a-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0c34a-169">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="0c34a-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0c34a-170">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c34a-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0c34a-171">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="0c34a-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0c34a-172">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0c34a-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0c34a-173">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0c34a-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0c34a-174">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="0c34a-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0c34a-175">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="0c34a-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0c34a-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="0c34a-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0c34a-177">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0c34a-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0c34a-178">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0c34a-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="0c34a-179">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0c34a-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0c34a-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c34a-180">RELATED LINKS</span></span>

