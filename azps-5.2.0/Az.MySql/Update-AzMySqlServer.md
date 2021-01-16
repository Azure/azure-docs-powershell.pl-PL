---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: b205f3d4eb9b1ebce360596714ea2524fb2e3be2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360194"
---
# <span data-ttu-id="bae7b-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="bae7b-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="bae7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bae7b-102">SYNOPSIS</span></span>
<span data-ttu-id="bae7b-103">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="bae7b-103">Updates an existing server.</span></span>
<span data-ttu-id="bae7b-104">Treść żądania może zawierać właściwości, które znajdują się w normalnej definicji serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="bae7b-105">Zamiast tego użyj Update-AzMySqlConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="bae7b-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="bae7b-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bae7b-106">SYNTAX</span></span>

### <span data-ttu-id="bae7b-107">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bae7b-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bae7b-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bae7b-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bae7b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="bae7b-109">DESCRIPTION</span></span>
<span data-ttu-id="bae7b-110">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="bae7b-110">Updates an existing server.</span></span>
<span data-ttu-id="bae7b-111">Treść żądania może zawierać właściwości, które znajdują się w normalnej definicji serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="bae7b-112">Zamiast tego użyj Update-AzMySqlConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="bae7b-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="bae7b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bae7b-113">EXAMPLES</span></span>

### <span data-ttu-id="bae7b-114">Przykład 1: aktualizowanie serwera MySql według grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="bae7b-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="bae7b-115">To polecenie cmdlet aktualizuje serwer MySql według grupy zasobów i nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="bae7b-116">Przykład 2: aktualizowanie serwera MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bae7b-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="bae7b-117">To polecenie cmdlet aktualizuje serwer MySql za pomocą tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bae7b-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="bae7b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bae7b-118">PARAMETERS</span></span>

### <span data-ttu-id="bae7b-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="bae7b-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="bae7b-120">Hasło logowania administratora.</span><span class="sxs-lookup"><span data-stu-id="bae7b-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="bae7b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bae7b-121">-AsJob</span></span>
<span data-ttu-id="bae7b-122">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="bae7b-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="bae7b-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="bae7b-123">-BackupRetentionDay</span></span>
<span data-ttu-id="bae7b-124">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-124">Backup retention days for the server.</span></span>
<span data-ttu-id="bae7b-125">Liczba dni jest z zakresu od 7 do 35.</span><span class="sxs-lookup"><span data-stu-id="bae7b-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="bae7b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bae7b-126">-DefaultProfile</span></span>
<span data-ttu-id="bae7b-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bae7b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bae7b-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bae7b-128">-InputObject</span></span>
<span data-ttu-id="bae7b-129">Parametr Identity.</span><span class="sxs-lookup"><span data-stu-id="bae7b-129">Identity Parameter.</span></span>
<span data-ttu-id="bae7b-130">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="bae7b-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bae7b-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bae7b-131">-Name</span></span>
<span data-ttu-id="bae7b-132">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-132">The name of the server.</span></span>

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

### <span data-ttu-id="bae7b-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bae7b-133">-NoWait</span></span>
<span data-ttu-id="bae7b-134">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="bae7b-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="bae7b-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="bae7b-135">-ReplicationRole</span></span>
<span data-ttu-id="bae7b-136">Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="bae7b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bae7b-137">-ResourceGroupName</span></span>
<span data-ttu-id="bae7b-138">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="bae7b-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bae7b-139">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="bae7b-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="bae7b-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="bae7b-140">-Sku</span></span>
<span data-ttu-id="bae7b-141">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bae7b-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="bae7b-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="bae7b-142">-SkuCapacity</span></span>
<span data-ttu-id="bae7b-143">Wydajność skalowalna/out przedstawiająca jednostki obliczeniowe serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="bae7b-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="bae7b-144">-SkuFamily</span></span>
<span data-ttu-id="bae7b-145">Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="bae7b-145">The family of hardware.</span></span>

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

### <span data-ttu-id="bae7b-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="bae7b-146">-SkuTier</span></span>
<span data-ttu-id="bae7b-147">Warstwa konkretnej jednostki SKU, na przykład podstawowa.</span><span class="sxs-lookup"><span data-stu-id="bae7b-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="bae7b-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="bae7b-148">-SslEnforcement</span></span>
<span data-ttu-id="bae7b-149">Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="bae7b-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="bae7b-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="bae7b-150">-StorageAutogrow</span></span>
<span data-ttu-id="bae7b-151">Włącz automatyczne zwiększanie przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="bae7b-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="bae7b-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="bae7b-152">-StorageInMb</span></span>
<span data-ttu-id="bae7b-153">Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="bae7b-154">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bae7b-154">-SubscriptionId</span></span>
<span data-ttu-id="bae7b-155">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bae7b-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="bae7b-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="bae7b-156">-Tag</span></span>
<span data-ttu-id="bae7b-157">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="bae7b-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="bae7b-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bae7b-158">-Confirm</span></span>
<span data-ttu-id="bae7b-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bae7b-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bae7b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bae7b-160">-WhatIf</span></span>
<span data-ttu-id="bae7b-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bae7b-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bae7b-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bae7b-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bae7b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bae7b-163">CommonParameters</span></span>
<span data-ttu-id="bae7b-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bae7b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bae7b-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bae7b-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bae7b-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bae7b-166">INPUTS</span></span>

### <span data-ttu-id="bae7b-167">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bae7b-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bae7b-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bae7b-168">OUTPUTS</span></span>

### <span data-ttu-id="bae7b-169">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="bae7b-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="bae7b-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bae7b-170">NOTES</span></span>

<span data-ttu-id="bae7b-171">PISUJE</span><span class="sxs-lookup"><span data-stu-id="bae7b-171">ALIASES</span></span>

<span data-ttu-id="bae7b-172">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bae7b-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bae7b-173">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bae7b-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bae7b-174">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bae7b-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bae7b-175">INPUTobject <IMySqlIdentity> : parametr Identity.</span><span class="sxs-lookup"><span data-stu-id="bae7b-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="bae7b-176">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bae7b-177">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bae7b-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bae7b-178">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bae7b-179">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bae7b-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bae7b-180">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-180">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="bae7b-181">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="bae7b-181">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bae7b-182">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bae7b-182">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bae7b-183">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="bae7b-183">The name is case insensitive.</span></span>
  - <span data-ttu-id="bae7b-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="bae7b-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bae7b-185">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bae7b-185">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bae7b-186">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="bae7b-186">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bae7b-187">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bae7b-187">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bae7b-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bae7b-188">RELATED LINKS</span></span>

