---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: 4b0d2f01336de83acbd904e08b0d0cbc62c0aca6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202178"
---
# <span data-ttu-id="cf09c-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="cf09c-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="cf09c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf09c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf09c-103">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="cf09c-103">Updates an existing server.</span></span>
<span data-ttu-id="cf09c-104">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="cf09c-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="cf09c-105">Użyj Update-AzPostSqlConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="cf09c-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="cf09c-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf09c-106">SYNTAX</span></span>

### <span data-ttu-id="cf09c-107">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="cf09c-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf09c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cf09c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf09c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf09c-109">DESCRIPTION</span></span>
<span data-ttu-id="cf09c-110">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="cf09c-110">Updates an existing server.</span></span>
<span data-ttu-id="cf09c-111">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="cf09c-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="cf09c-112">Użyj Update-AzPostSqlConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="cf09c-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="cf09c-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf09c-113">EXAMPLES</span></span>

### <span data-ttu-id="cf09c-114">Przykład 1. Aktualizowanie serwera PostgreSql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="cf09c-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="cf09c-115">To polecenie cmdlet aktualizuje serwer PostgreSql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="cf09c-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="cf09c-116">Przykład 2. Aktualizowanie serwera PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="cf09c-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="cf09c-117">To polecenie cmdlet aktualizuje serwer PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="cf09c-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="cf09c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf09c-118">PARAMETERS</span></span>

### <span data-ttu-id="cf09c-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="cf09c-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="cf09c-120">Hasło logowania administratora.</span><span class="sxs-lookup"><span data-stu-id="cf09c-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="cf09c-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cf09c-121">-AsJob</span></span>
<span data-ttu-id="cf09c-122">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="cf09c-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="cf09c-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="cf09c-123">-BackupRetentionDay</span></span>
<span data-ttu-id="cf09c-124">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="cf09c-124">Backup retention days for the server.</span></span>
<span data-ttu-id="cf09c-125">Liczba dni wynosi od 7 do 35.</span><span class="sxs-lookup"><span data-stu-id="cf09c-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="cf09c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf09c-126">-DefaultProfile</span></span>
<span data-ttu-id="cf09c-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf09c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf09c-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf09c-128">-InputObject</span></span>
<span data-ttu-id="cf09c-129">Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="cf09c-129">Identity Parameter.</span></span>
<span data-ttu-id="cf09c-130">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="cf09c-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf09c-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="cf09c-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="cf09c-132">Ustaw minimalną wersję protokołu TLS dla połączeń z serwerem, gdy jest włączony protokół SSL.</span><span class="sxs-lookup"><span data-stu-id="cf09c-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="cf09c-133">Wartości domyślne to TLSEnforcementDisabled.accepted wartości: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="cf09c-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf09c-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cf09c-134">-Name</span></span>
<span data-ttu-id="cf09c-135">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="cf09c-135">The name of the server.</span></span>

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

### <span data-ttu-id="cf09c-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cf09c-136">-NoWait</span></span>
<span data-ttu-id="cf09c-137">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="cf09c-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="cf09c-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="cf09c-138">-ReplicationRole</span></span>
<span data-ttu-id="cf09c-139">Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="cf09c-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="cf09c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf09c-140">-ResourceGroupName</span></span>
<span data-ttu-id="cf09c-141">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="cf09c-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cf09c-142">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="cf09c-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cf09c-143">- SKU</span><span class="sxs-lookup"><span data-stu-id="cf09c-143">-Sku</span></span>
<span data-ttu-id="cf09c-144">Nazwa sKU, zwykle warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cf09c-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="cf09c-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="cf09c-145">-SkuCapacity</span></span>
<span data-ttu-id="cf09c-146">Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.</span><span class="sxs-lookup"><span data-stu-id="cf09c-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="cf09c-147">- SKUFamily</span><span class="sxs-lookup"><span data-stu-id="cf09c-147">-SkuFamily</span></span>
<span data-ttu-id="cf09c-148">Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="cf09c-148">The family of hardware.</span></span>

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

### <span data-ttu-id="cf09c-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="cf09c-149">-SkuTier</span></span>
<span data-ttu-id="cf09c-150">Warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="cf09c-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="cf09c-151">- SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="cf09c-151">-SslEnforcement</span></span>
<span data-ttu-id="cf09c-152">Włączanie wymuszania ssl lub nie w przypadku nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="cf09c-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="cf09c-153">- StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="cf09c-153">-StorageAutogrow</span></span>
<span data-ttu-id="cf09c-154">Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf09c-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="cf09c-155">- StorageInMb</span><span class="sxs-lookup"><span data-stu-id="cf09c-155">-StorageInMb</span></span>
<span data-ttu-id="cf09c-156">Maksymalna dozwolona ilość miejsca do magazynowania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="cf09c-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="cf09c-157">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf09c-157">-SubscriptionId</span></span>
<span data-ttu-id="cf09c-158">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf09c-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="cf09c-159">— Tag</span><span class="sxs-lookup"><span data-stu-id="cf09c-159">-Tag</span></span>
<span data-ttu-id="cf09c-160">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="cf09c-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="cf09c-161">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf09c-161">-Confirm</span></span>
<span data-ttu-id="cf09c-162">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf09c-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf09c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf09c-163">-WhatIf</span></span>
<span data-ttu-id="cf09c-164">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf09c-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf09c-165">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cf09c-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf09c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf09c-166">CommonParameters</span></span>
<span data-ttu-id="cf09c-167">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf09c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf09c-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf09c-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf09c-169">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf09c-169">INPUTS</span></span>

### <span data-ttu-id="cf09c-170">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cf09c-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="cf09c-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf09c-171">OUTPUTS</span></span>

### <span data-ttu-id="cf09c-172">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="cf09c-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="cf09c-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf09c-173">NOTES</span></span>

<span data-ttu-id="cf09c-174">ALIASY</span><span class="sxs-lookup"><span data-stu-id="cf09c-174">ALIASES</span></span>

<span data-ttu-id="cf09c-175">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="cf09c-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf09c-176">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cf09c-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf09c-177">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf09c-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf09c-178">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="cf09c-178">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="cf09c-179">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="cf09c-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cf09c-180">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="cf09c-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cf09c-181">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="cf09c-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cf09c-182">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cf09c-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf09c-183">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cf09c-183">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cf09c-184">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf09c-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cf09c-185">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="cf09c-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="cf09c-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="cf09c-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cf09c-187">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="cf09c-187">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cf09c-188">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="cf09c-188">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cf09c-189">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cf09c-189">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cf09c-190">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf09c-190">RELATED LINKS</span></span>

