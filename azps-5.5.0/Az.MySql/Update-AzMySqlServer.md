---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: 6168c557e3ae3a417f4c04195e6ef166ea3a01d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190026"
---
# <span data-ttu-id="bd8e6-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="bd8e6-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="bd8e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8e6-103">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-103">Updates an existing server.</span></span>
<span data-ttu-id="bd8e6-104">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="bd8e6-105">Użyj Update-AzMySqlConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="bd8e6-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bd8e6-106">SYNTAX</span></span>

### <span data-ttu-id="bd8e6-107">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="bd8e6-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bd8e6-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bd8e6-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd8e6-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="bd8e6-109">DESCRIPTION</span></span>
<span data-ttu-id="bd8e6-110">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-110">Updates an existing server.</span></span>
<span data-ttu-id="bd8e6-111">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="bd8e6-112">Użyj Update-AzMySqlConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="bd8e6-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bd8e6-113">EXAMPLES</span></span>

### <span data-ttu-id="bd8e6-114">Przykład 1. Aktualizowanie serwera MySql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="bd8e6-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="bd8e6-115">To polecenie cmdlet aktualizuje serwer MySql według nazwy serwera i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="bd8e6-116">Przykład 2. Aktualizowanie serwera MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="bd8e6-117">To polecenie cmdlet aktualizuje serwer MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="bd8e6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd8e6-118">PARAMETERS</span></span>

### <span data-ttu-id="bd8e6-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="bd8e6-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="bd8e6-120">Hasło logowania administratora.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="bd8e6-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bd8e6-121">-AsJob</span></span>
<span data-ttu-id="bd8e6-122">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="bd8e6-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="bd8e6-123">-BackupRetentionDay</span></span>
<span data-ttu-id="bd8e6-124">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-124">Backup retention days for the server.</span></span>
<span data-ttu-id="bd8e6-125">Liczba dni wynosi między 7 a 35.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="bd8e6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd8e6-126">-DefaultProfile</span></span>
<span data-ttu-id="bd8e6-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd8e6-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd8e6-128">-InputObject</span></span>
<span data-ttu-id="bd8e6-129">Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-129">Identity Parameter.</span></span>
<span data-ttu-id="bd8e6-130">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bd8e6-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="bd8e6-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="bd8e6-132">Ustaw minimalną wersję protokołu TLS dla połączeń z serwerem, gdy jest włączony protokół SSL.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="bd8e6-133">Wartości domyślne to TLSEnforcementDisabled.accepted: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8e6-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bd8e6-134">-Name</span></span>
<span data-ttu-id="bd8e6-135">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-135">The name of the server.</span></span>

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

### <span data-ttu-id="bd8e6-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bd8e6-136">-NoWait</span></span>
<span data-ttu-id="bd8e6-137">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="bd8e6-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="bd8e6-138">-ReplicationRole</span></span>
<span data-ttu-id="bd8e6-139">Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="bd8e6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd8e6-140">-ResourceGroupName</span></span>
<span data-ttu-id="bd8e6-141">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bd8e6-142">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="bd8e6-143">- SKU</span><span class="sxs-lookup"><span data-stu-id="bd8e6-143">-Sku</span></span>
<span data-ttu-id="bd8e6-144">Nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="bd8e6-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="bd8e6-145">-SkuCapacity</span></span>
<span data-ttu-id="bd8e6-146">Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="bd8e6-147">- SKUFamily</span><span class="sxs-lookup"><span data-stu-id="bd8e6-147">-SkuFamily</span></span>
<span data-ttu-id="bd8e6-148">Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-148">The family of hardware.</span></span>

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

### <span data-ttu-id="bd8e6-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="bd8e6-149">-SkuTier</span></span>
<span data-ttu-id="bd8e6-150">Warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-150">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8e6-151">- SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="bd8e6-151">-SslEnforcement</span></span>
<span data-ttu-id="bd8e6-152">Włączanie wymuszania ssl lub nie w przypadku nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-152">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8e6-153">- StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="bd8e6-153">-StorageAutogrow</span></span>
<span data-ttu-id="bd8e6-154">Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-154">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8e6-155">- StorageInMb</span><span class="sxs-lookup"><span data-stu-id="bd8e6-155">-StorageInMb</span></span>
<span data-ttu-id="bd8e6-156">Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="bd8e6-157">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd8e6-157">-SubscriptionId</span></span>
<span data-ttu-id="bd8e6-158">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="bd8e6-159">— Tag</span><span class="sxs-lookup"><span data-stu-id="bd8e6-159">-Tag</span></span>
<span data-ttu-id="bd8e6-160">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="bd8e6-161">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd8e6-161">-Confirm</span></span>
<span data-ttu-id="bd8e6-162">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd8e6-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd8e6-163">-WhatIf</span></span>
<span data-ttu-id="bd8e6-164">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd8e6-165">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd8e6-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8e6-166">CommonParameters</span></span>
<span data-ttu-id="bd8e6-167">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8e6-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd8e6-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8e6-169">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd8e6-169">INPUTS</span></span>

### <span data-ttu-id="bd8e6-170">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bd8e6-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bd8e6-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd8e6-171">OUTPUTS</span></span>

### <span data-ttu-id="bd8e6-172">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iServer</span><span class="sxs-lookup"><span data-stu-id="bd8e6-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="bd8e6-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bd8e6-173">NOTES</span></span>

<span data-ttu-id="bd8e6-174">ALIASY</span><span class="sxs-lookup"><span data-stu-id="bd8e6-174">ALIASES</span></span>

<span data-ttu-id="bd8e6-175">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="bd8e6-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd8e6-176">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd8e6-177">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd8e6-178">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-178">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="bd8e6-179">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bd8e6-180">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bd8e6-181">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bd8e6-182">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bd8e6-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bd8e6-183">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-183">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="bd8e6-184">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bd8e6-185">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bd8e6-186">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="bd8e6-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bd8e6-188">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bd8e6-189">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bd8e6-190">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bd8e6-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bd8e6-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd8e6-191">RELATED LINKS</span></span>

