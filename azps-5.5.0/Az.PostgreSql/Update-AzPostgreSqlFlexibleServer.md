---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: f6634f83e89abe4c775779c052ad9ee7b21bea6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184002"
---
# <span data-ttu-id="857ad-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="857ad-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="857ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="857ad-102">SYNOPSIS</span></span>
<span data-ttu-id="857ad-103">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="857ad-103">Updates an existing server.</span></span>
<span data-ttu-id="857ad-104">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="857ad-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="857ad-105">Użyj Update-AzPostSqlFlexibleServerConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="857ad-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="857ad-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="857ad-106">SYNTAX</span></span>

### <span data-ttu-id="857ad-107">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="857ad-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="857ad-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="857ad-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="857ad-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="857ad-109">DESCRIPTION</span></span>
<span data-ttu-id="857ad-110">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="857ad-110">Updates an existing server.</span></span>
<span data-ttu-id="857ad-111">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="857ad-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="857ad-112">Użyj Update-AzPostgreSqlFlexibleServerConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="857ad-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="857ad-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="857ad-113">EXAMPLES</span></span>

### <span data-ttu-id="857ad-114">Przykład 1. Aktualizowanie serwera PostgreSql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="857ad-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="857ad-115">To polecenie cmdlet aktualizuje serwer PostgreSql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="857ad-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="857ad-116">Przykład 2. Aktualizowanie serwera PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="857ad-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="857ad-117">To polecenie cmdlet aktualizuje serwer PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="857ad-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="857ad-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="857ad-118">PARAMETERS</span></span>

### <span data-ttu-id="857ad-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="857ad-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="857ad-120">Hasło logowania administratora.</span><span class="sxs-lookup"><span data-stu-id="857ad-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="857ad-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="857ad-121">-AsJob</span></span>
<span data-ttu-id="857ad-122">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="857ad-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="857ad-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="857ad-123">-BackupRetentionDay</span></span>
<span data-ttu-id="857ad-124">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="857ad-124">Backup retention days for the server.</span></span>
<span data-ttu-id="857ad-125">Liczba dni wynosi między 7 a 35.</span><span class="sxs-lookup"><span data-stu-id="857ad-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="857ad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857ad-126">-DefaultProfile</span></span>
<span data-ttu-id="857ad-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="857ad-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="857ad-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="857ad-128">-HaEnabled</span></span>
<span data-ttu-id="857ad-129">Włączanie lub wyłączanie funkcji wysokiej dostępności.</span><span class="sxs-lookup"><span data-stu-id="857ad-129">Enable or disable high availability feature.</span></span>

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

### <span data-ttu-id="857ad-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="857ad-130">-InputObject</span></span>
<span data-ttu-id="857ad-131">Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="857ad-131">Identity Parameter.</span></span>
<span data-ttu-id="857ad-132">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="857ad-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="857ad-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="857ad-133">-Name</span></span>
<span data-ttu-id="857ad-134">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="857ad-134">The name of the server.</span></span>

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

### <span data-ttu-id="857ad-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="857ad-135">-NoWait</span></span>
<span data-ttu-id="857ad-136">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="857ad-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="857ad-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="857ad-137">-ReplicationRole</span></span>
<span data-ttu-id="857ad-138">Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="857ad-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="857ad-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857ad-139">-ResourceGroupName</span></span>
<span data-ttu-id="857ad-140">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="857ad-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="857ad-141">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="857ad-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="857ad-142">- SKU</span><span class="sxs-lookup"><span data-stu-id="857ad-142">-Sku</span></span>
<span data-ttu-id="857ad-143">Nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="857ad-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="857ad-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="857ad-144">-SkuTier</span></span>
<span data-ttu-id="857ad-145">Warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="857ad-145">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="857ad-146">- SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="857ad-146">-SslEnforcement</span></span>
<span data-ttu-id="857ad-147">Włączanie wymuszania ssl lub nie w przypadku nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="857ad-147">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="857ad-148">- StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="857ad-148">-StorageAutogrow</span></span>
<span data-ttu-id="857ad-149">Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="857ad-149">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="857ad-150">- StorageInMb</span><span class="sxs-lookup"><span data-stu-id="857ad-150">-StorageInMb</span></span>
<span data-ttu-id="857ad-151">Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="857ad-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="857ad-152">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="857ad-152">-SubscriptionId</span></span>
<span data-ttu-id="857ad-153">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="857ad-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="857ad-154">— Tag</span><span class="sxs-lookup"><span data-stu-id="857ad-154">-Tag</span></span>
<span data-ttu-id="857ad-155">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="857ad-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="857ad-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="857ad-156">-Confirm</span></span>
<span data-ttu-id="857ad-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="857ad-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="857ad-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="857ad-158">-WhatIf</span></span>
<span data-ttu-id="857ad-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="857ad-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="857ad-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="857ad-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="857ad-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857ad-161">CommonParameters</span></span>
<span data-ttu-id="857ad-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="857ad-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857ad-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="857ad-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857ad-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="857ad-164">INPUTS</span></span>

### <span data-ttu-id="857ad-165">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="857ad-165">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="857ad-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="857ad-166">OUTPUTS</span></span>

### <span data-ttu-id="857ad-167">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="857ad-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="857ad-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="857ad-168">NOTES</span></span>

<span data-ttu-id="857ad-169">ALIASY</span><span class="sxs-lookup"><span data-stu-id="857ad-169">ALIASES</span></span>

<span data-ttu-id="857ad-170">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="857ad-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="857ad-171">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="857ad-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="857ad-172">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="857ad-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="857ad-173">INPUTOBJECT: <IPostgreSqlIdentity> Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="857ad-173">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="857ad-174">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="857ad-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="857ad-175">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="857ad-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="857ad-176">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="857ad-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="857ad-177">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="857ad-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="857ad-178">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="857ad-178">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="857ad-179">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="857ad-179">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="857ad-180">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="857ad-180">The name is case insensitive.</span></span>
  - <span data-ttu-id="857ad-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="857ad-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="857ad-182">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="857ad-182">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="857ad-183">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="857ad-183">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="857ad-184">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="857ad-184">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="857ad-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="857ad-185">RELATED LINKS</span></span>

