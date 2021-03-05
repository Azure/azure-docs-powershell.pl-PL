---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 65004c35ffa9c4cb227845787c91219a319789fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974666"
---
# <span data-ttu-id="8698e-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="8698e-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="8698e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8698e-102">SYNOPSIS</span></span>
<span data-ttu-id="8698e-103">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="8698e-103">Updates an existing server.</span></span>
<span data-ttu-id="8698e-104">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="8698e-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8698e-105">Użyj Update-AzPostSqlFlexibleServerConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="8698e-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8698e-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8698e-106">SYNTAX</span></span>

### <span data-ttu-id="8698e-107">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="8698e-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8698e-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8698e-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8698e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="8698e-109">DESCRIPTION</span></span>
<span data-ttu-id="8698e-110">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="8698e-110">Updates an existing server.</span></span>
<span data-ttu-id="8698e-111">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="8698e-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8698e-112">Użyj Update-AzPostgreSqlFlexibleServerConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="8698e-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8698e-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8698e-113">EXAMPLES</span></span>

### <span data-ttu-id="8698e-114">Przykład 1. Aktualizowanie serwera PostgreSql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="8698e-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="8698e-115">To polecenie cmdlet aktualizuje serwer PostgreSql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="8698e-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="8698e-116">Przykład 2. Aktualizowanie serwera PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="8698e-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="8698e-117">To polecenie cmdlet aktualizuje serwer PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="8698e-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="8698e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8698e-118">PARAMETERS</span></span>

### <span data-ttu-id="8698e-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="8698e-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="8698e-120">Hasło logowania administratora.</span><span class="sxs-lookup"><span data-stu-id="8698e-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="8698e-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8698e-121">-AsJob</span></span>
<span data-ttu-id="8698e-122">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="8698e-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="8698e-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="8698e-123">-BackupRetentionDay</span></span>
<span data-ttu-id="8698e-124">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="8698e-124">Backup retention days for the server.</span></span>
<span data-ttu-id="8698e-125">Liczba dni wynosi między 7 a 35.</span><span class="sxs-lookup"><span data-stu-id="8698e-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="8698e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8698e-126">-DefaultProfile</span></span>
<span data-ttu-id="8698e-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8698e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8698e-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="8698e-128">-HaEnabled</span></span>
<span data-ttu-id="8698e-129">Włączanie lub wyłączanie funkcji wysokiej dostępności.</span><span class="sxs-lookup"><span data-stu-id="8698e-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8698e-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8698e-130">-InputObject</span></span>
<span data-ttu-id="8698e-131">Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="8698e-131">Identity Parameter.</span></span>
<span data-ttu-id="8698e-132">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="8698e-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8698e-133">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="8698e-133">-MaintenanceWindow</span></span>
<span data-ttu-id="8698e-134">Okres czasu (UTC) wyznaczonego na konserwację.</span><span class="sxs-lookup"><span data-stu-id="8698e-134">Period of time (UTC) designated for maintenance.</span></span>
<span data-ttu-id="8698e-135">Przykłady: "Nie:23:30", aby zaplanować na niedzielę o godzinie 23:30 czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="8698e-135">Examples: "Sun:23:30" to schedule on Sunday, 11:30pm UTC.</span></span>
<span data-ttu-id="8698e-136">Aby wrócić do domyślnego przekazania w trybie "Wyłączone"</span><span class="sxs-lookup"><span data-stu-id="8698e-136">To set back to default pass in "Disabled"</span></span>

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

### <span data-ttu-id="8698e-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8698e-137">-Name</span></span>
<span data-ttu-id="8698e-138">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8698e-138">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8698e-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8698e-139">-NoWait</span></span>
<span data-ttu-id="8698e-140">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="8698e-140">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8698e-141">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="8698e-141">-ReplicationRole</span></span>
<span data-ttu-id="8698e-142">Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="8698e-142">The replication role of the server.</span></span>

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

### <span data-ttu-id="8698e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8698e-143">-ResourceGroupName</span></span>
<span data-ttu-id="8698e-144">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="8698e-144">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8698e-145">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="8698e-145">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8698e-146">- SKU</span><span class="sxs-lookup"><span data-stu-id="8698e-146">-Sku</span></span>
<span data-ttu-id="8698e-147">Nazwa sKU, np. Burstable_B1ms, Standard_D2ds_v4</span><span class="sxs-lookup"><span data-stu-id="8698e-147">The name of the sku, e.g. Burstable_B1ms, Standard_D2ds_v4</span></span>

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

### <span data-ttu-id="8698e-148">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8698e-148">-SkuTier</span></span>
<span data-ttu-id="8698e-149">Warstwa określonej sku.</span><span class="sxs-lookup"><span data-stu-id="8698e-149">The tier of the particular SKU.</span></span>
<span data-ttu-id="8698e-150">Zaakceptowane wartości: Zbędna seria, OgólnePozyska, Zoptymalizowana pamięć.</span><span class="sxs-lookup"><span data-stu-id="8698e-150">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="8698e-151">Domyślne: Zamieć na serio.</span><span class="sxs-lookup"><span data-stu-id="8698e-151">Default: Burstable.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8698e-152">- SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="8698e-152">-SslEnforcement</span></span>
<span data-ttu-id="8698e-153">Włączanie wymuszania ssl lub nie w przypadku nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="8698e-153">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8698e-154">- StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="8698e-154">-StorageAutogrow</span></span>
<span data-ttu-id="8698e-155">Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="8698e-155">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8698e-156">- StorageInMb</span><span class="sxs-lookup"><span data-stu-id="8698e-156">-StorageInMb</span></span>
<span data-ttu-id="8698e-157">Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8698e-157">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="8698e-158">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8698e-158">-SubscriptionId</span></span>
<span data-ttu-id="8698e-159">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8698e-159">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8698e-160">— Tag</span><span class="sxs-lookup"><span data-stu-id="8698e-160">-Tag</span></span>
<span data-ttu-id="8698e-161">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="8698e-161">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8698e-162">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8698e-162">-Confirm</span></span>
<span data-ttu-id="8698e-163">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8698e-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8698e-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8698e-164">-WhatIf</span></span>
<span data-ttu-id="8698e-165">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8698e-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8698e-166">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8698e-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8698e-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8698e-167">CommonParameters</span></span>
<span data-ttu-id="8698e-168">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8698e-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8698e-169">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8698e-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8698e-170">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8698e-170">INPUTS</span></span>

### <span data-ttu-id="8698e-171">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8698e-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="8698e-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8698e-172">OUTPUTS</span></span>

### <span data-ttu-id="8698e-173">Microsoft.Azure.PowerShell.cmdlet.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="8698e-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="8698e-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8698e-174">NOTES</span></span>

<span data-ttu-id="8698e-175">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8698e-175">ALIASES</span></span>

<span data-ttu-id="8698e-176">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8698e-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8698e-177">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8698e-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8698e-178">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8698e-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8698e-179">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="8698e-179">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="8698e-180">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="8698e-180">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8698e-181">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8698e-181">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8698e-182">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="8698e-182">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8698e-183">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8698e-183">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8698e-184">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8698e-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8698e-185">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8698e-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8698e-186">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="8698e-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="8698e-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="8698e-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8698e-188">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8698e-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8698e-189">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8698e-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8698e-190">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8698e-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8698e-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8698e-191">RELATED LINKS</span></span>

