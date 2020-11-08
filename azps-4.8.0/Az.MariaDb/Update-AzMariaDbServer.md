---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064020"
---
# <span data-ttu-id="70fdb-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="70fdb-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="70fdb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="70fdb-103">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="70fdb-103">Updates an existing server.</span></span>
<span data-ttu-id="70fdb-104">Treść żądania może zawierać właściwości, które znajdują się w normalnej definicji serwera.</span><span class="sxs-lookup"><span data-stu-id="70fdb-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="70fdb-105">Zamiast tego użyj Update-AzMariaDbConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="70fdb-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="70fdb-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70fdb-106">SYNTAX</span></span>

### <span data-ttu-id="70fdb-107">Nazwa_serwera (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="70fdb-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70fdb-108">Serverobject</span><span class="sxs-lookup"><span data-stu-id="70fdb-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="70fdb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="70fdb-109">DESCRIPTION</span></span>
<span data-ttu-id="70fdb-110">Aktualizuje istniejący serwer.</span><span class="sxs-lookup"><span data-stu-id="70fdb-110">Updates an existing server.</span></span>
<span data-ttu-id="70fdb-111">Treść żądania może zawierać właściwości, które znajdują się w normalnej definicji serwera.</span><span class="sxs-lookup"><span data-stu-id="70fdb-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="70fdb-112">Zamiast tego użyj Update-AzMariaDbConfiguration, jeśli chcesz zaktualizować parametry serwera, takie jak wait_timeout lub net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="70fdb-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="70fdb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70fdb-113">EXAMPLES</span></span>

### <span data-ttu-id="70fdb-114">Przykład 1: Aktualizacja MariaDB</span><span class="sxs-lookup"><span data-stu-id="70fdb-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="70fdb-115">To polecenie aktualizuje MariaDB.</span><span class="sxs-lookup"><span data-stu-id="70fdb-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="70fdb-116">Przykład 2: Aktualizacja MariaDB</span><span class="sxs-lookup"><span data-stu-id="70fdb-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="70fdb-117">To polecenie aktualizuje MariaDB.</span><span class="sxs-lookup"><span data-stu-id="70fdb-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="70fdb-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70fdb-118">PARAMETERS</span></span>

### <span data-ttu-id="70fdb-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="70fdb-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="70fdb-120">Hasło logowania administratora.</span><span class="sxs-lookup"><span data-stu-id="70fdb-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="70fdb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70fdb-121">-AsJob</span></span>
<span data-ttu-id="70fdb-122">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="70fdb-122">Run the command as a job</span></span>

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

### <span data-ttu-id="70fdb-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="70fdb-123">-BackupRetentionDay</span></span>
<span data-ttu-id="70fdb-124">Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="70fdb-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="70fdb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70fdb-125">-DefaultProfile</span></span>
<span data-ttu-id="70fdb-126">Region DefaultParameters poświadczenia, konto, dzierżawca i abonament używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70fdb-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70fdb-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="70fdb-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="70fdb-128">Włącz lokalizację geograficzną lub niezbędną dla kopii zapasowych serwera.</span><span class="sxs-lookup"><span data-stu-id="70fdb-128">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="70fdb-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="70fdb-129">-InputObject</span></span>
<span data-ttu-id="70fdb-130">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="70fdb-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="70fdb-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70fdb-131">-Name</span></span>
<span data-ttu-id="70fdb-132">Nazwa serwera MariaDB</span><span class="sxs-lookup"><span data-stu-id="70fdb-132">MariaDB server name</span></span>

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

### <span data-ttu-id="70fdb-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="70fdb-133">-NoWait</span></span>
<span data-ttu-id="70fdb-134">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="70fdb-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="70fdb-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="70fdb-135">-ReplicationRole</span></span>
<span data-ttu-id="70fdb-136">Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="70fdb-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="70fdb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70fdb-137">-ResourceGroupName</span></span>
<span data-ttu-id="70fdb-138">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="70fdb-138">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="70fdb-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="70fdb-139">-Sku</span></span>
<span data-ttu-id="70fdb-140">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="70fdb-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="70fdb-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="70fdb-141">-SslEnforcement</span></span>
<span data-ttu-id="70fdb-142">Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="70fdb-142">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="70fdb-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="70fdb-143">-StorageAutogrow</span></span>
<span data-ttu-id="70fdb-144">Włącz automatyczne zwiększanie przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="70fdb-144">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="70fdb-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="70fdb-145">-StorageInMb</span></span>
<span data-ttu-id="70fdb-146">Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="70fdb-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="70fdb-147">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="70fdb-147">-SubscriptionId</span></span>
<span data-ttu-id="70fdb-148">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą</span><span class="sxs-lookup"><span data-stu-id="70fdb-148">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="70fdb-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="70fdb-149">-Tag</span></span>
<span data-ttu-id="70fdb-150">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="70fdb-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="70fdb-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70fdb-151">-Confirm</span></span>
<span data-ttu-id="70fdb-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70fdb-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70fdb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70fdb-153">-WhatIf</span></span>
<span data-ttu-id="70fdb-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70fdb-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70fdb-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70fdb-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70fdb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fdb-156">CommonParameters</span></span>
<span data-ttu-id="70fdb-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70fdb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fdb-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70fdb-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fdb-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70fdb-159">INPUTS</span></span>

### <span data-ttu-id="70fdb-160">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="70fdb-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="70fdb-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70fdb-161">OUTPUTS</span></span>

### <span data-ttu-id="70fdb-162">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="70fdb-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="70fdb-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70fdb-163">NOTES</span></span>

<span data-ttu-id="70fdb-164">PISUJE</span><span class="sxs-lookup"><span data-stu-id="70fdb-164">ALIASES</span></span>

<span data-ttu-id="70fdb-165">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70fdb-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="70fdb-166">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="70fdb-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70fdb-167">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="70fdb-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="70fdb-168">INPUTobject <IMariaDbIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="70fdb-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="70fdb-169">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="70fdb-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="70fdb-170">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70fdb-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="70fdb-171">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="70fdb-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="70fdb-172">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="70fdb-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="70fdb-173">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="70fdb-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="70fdb-174">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="70fdb-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="70fdb-175">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="70fdb-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="70fdb-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="70fdb-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="70fdb-177">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="70fdb-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="70fdb-178">`[SubscriptionId <String>]`: Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70fdb-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="70fdb-179">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="70fdb-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="70fdb-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70fdb-180">RELATED LINKS</span></span>

