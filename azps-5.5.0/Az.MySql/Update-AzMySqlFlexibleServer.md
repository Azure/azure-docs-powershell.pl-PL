---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3e1f79f431e5f0ff5c39c03a7f3c41a20c2543e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180027"
---
# <span data-ttu-id="de8d7-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="de8d7-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="de8d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de8d7-102">SYNOPSIS</span></span>
<span data-ttu-id="de8d7-103">Aktualizuje istniejący serwer elastyczny MySQL.</span><span class="sxs-lookup"><span data-stu-id="de8d7-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="de8d7-104">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="de8d7-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="de8d7-105">Użyj Update-AzMySqlFlexibleServerConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="de8d7-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="de8d7-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de8d7-106">SYNTAX</span></span>

### <span data-ttu-id="de8d7-107">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="de8d7-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="de8d7-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="de8d7-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de8d7-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="de8d7-109">DESCRIPTION</span></span>
<span data-ttu-id="de8d7-110">Aktualizuje istniejący serwer elastyczny MySQL.</span><span class="sxs-lookup"><span data-stu-id="de8d7-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="de8d7-111">Treść żądania może zawierać jedną lub wiele właściwości zawartych w definicji serwera normalnego.</span><span class="sxs-lookup"><span data-stu-id="de8d7-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="de8d7-112">Użyj Update-AzMySqlFlexibleServerConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="de8d7-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="de8d7-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de8d7-113">EXAMPLES</span></span>

### <span data-ttu-id="de8d7-114">Przykład 1. Aktualizowanie serwera MySql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="de8d7-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="de8d7-115">To polecenie cmdlet aktualizuje serwer MySql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="de8d7-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="de8d7-116">Przykład 2. Aktualizowanie serwera MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="de8d7-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="de8d7-117">To polecenie cmdlet aktualizuje serwer MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="de8d7-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="de8d7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de8d7-118">PARAMETERS</span></span>

### <span data-ttu-id="de8d7-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="de8d7-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="de8d7-120">Hasło logowania administratora.</span><span class="sxs-lookup"><span data-stu-id="de8d7-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="de8d7-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="de8d7-121">-AsJob</span></span>
<span data-ttu-id="de8d7-122">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="de8d7-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="de8d7-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="de8d7-123">-BackupRetentionDay</span></span>
<span data-ttu-id="de8d7-124">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="de8d7-124">Backup retention days for the server.</span></span>
<span data-ttu-id="de8d7-125">Liczba dni wynosi między 7 a 35.</span><span class="sxs-lookup"><span data-stu-id="de8d7-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="de8d7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8d7-126">-DefaultProfile</span></span>
<span data-ttu-id="de8d7-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de8d7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de8d7-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="de8d7-128">-HaEnabled</span></span>
<span data-ttu-id="de8d7-129">Włączanie lub wyłączanie funkcji wysokiej dostępności.</span><span class="sxs-lookup"><span data-stu-id="de8d7-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8d7-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de8d7-130">-InputObject</span></span>
<span data-ttu-id="de8d7-131">Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="de8d7-131">Identity Parameter.</span></span>
<span data-ttu-id="de8d7-132">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="de8d7-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="de8d7-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="de8d7-133">-Name</span></span>
<span data-ttu-id="de8d7-134">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="de8d7-134">The name of the server.</span></span>

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

### <span data-ttu-id="de8d7-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="de8d7-135">-NoWait</span></span>
<span data-ttu-id="de8d7-136">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="de8d7-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="de8d7-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="de8d7-137">-ReplicationRole</span></span>
<span data-ttu-id="de8d7-138">Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="de8d7-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="de8d7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de8d7-139">-ResourceGroupName</span></span>
<span data-ttu-id="de8d7-140">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="de8d7-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="de8d7-141">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="de8d7-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="de8d7-142">- SKU</span><span class="sxs-lookup"><span data-stu-id="de8d7-142">-Sku</span></span>
<span data-ttu-id="de8d7-143">Nazwa sKU, zwykle warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="de8d7-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="de8d7-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="de8d7-144">-SkuTier</span></span>
<span data-ttu-id="de8d7-145">Warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="de8d7-145">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="de8d7-146">- SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="de8d7-146">-SslEnforcement</span></span>
<span data-ttu-id="de8d7-147">Włączanie wymuszania ssl lub nie w przypadku nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="de8d7-147">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="de8d7-148">- StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="de8d7-148">-StorageAutogrow</span></span>
<span data-ttu-id="de8d7-149">Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="de8d7-149">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="de8d7-150">- StorageInMb</span><span class="sxs-lookup"><span data-stu-id="de8d7-150">-StorageInMb</span></span>
<span data-ttu-id="de8d7-151">Maksymalna dozwolona ilość miejsca do magazynowania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="de8d7-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="de8d7-152">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de8d7-152">-SubscriptionId</span></span>
<span data-ttu-id="de8d7-153">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="de8d7-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="de8d7-154">— Tag</span><span class="sxs-lookup"><span data-stu-id="de8d7-154">-Tag</span></span>
<span data-ttu-id="de8d7-155">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="de8d7-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="de8d7-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de8d7-156">-Confirm</span></span>
<span data-ttu-id="de8d7-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="de8d7-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de8d7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de8d7-158">-WhatIf</span></span>
<span data-ttu-id="de8d7-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de8d7-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de8d7-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="de8d7-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de8d7-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8d7-161">CommonParameters</span></span>
<span data-ttu-id="de8d7-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de8d7-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8d7-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de8d7-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8d7-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de8d7-164">INPUTS</span></span>

### <span data-ttu-id="de8d7-165">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="de8d7-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="de8d7-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de8d7-166">OUTPUTS</span></span>

### <span data-ttu-id="de8d7-167">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="de8d7-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="de8d7-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de8d7-168">NOTES</span></span>

<span data-ttu-id="de8d7-169">ALIASY</span><span class="sxs-lookup"><span data-stu-id="de8d7-169">ALIASES</span></span>

<span data-ttu-id="de8d7-170">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="de8d7-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="de8d7-171">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="de8d7-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de8d7-172">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="de8d7-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="de8d7-173">INPUTOBJECT: <IMySqlIdentity> Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="de8d7-173">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="de8d7-174">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="de8d7-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="de8d7-175">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="de8d7-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="de8d7-176">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="de8d7-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="de8d7-177">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="de8d7-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="de8d7-178">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="de8d7-178">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="de8d7-179">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="de8d7-179">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="de8d7-180">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="de8d7-180">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="de8d7-181">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="de8d7-181">The name is case insensitive.</span></span>
  - <span data-ttu-id="de8d7-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="de8d7-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="de8d7-183">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="de8d7-183">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="de8d7-184">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="de8d7-184">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="de8d7-185">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="de8d7-185">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="de8d7-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de8d7-186">RELATED LINKS</span></span>

