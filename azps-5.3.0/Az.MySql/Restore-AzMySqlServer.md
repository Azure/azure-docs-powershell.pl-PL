---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 7a53cefa9aca7e4ea679b31763c19e82d4d1e841
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498897"
---
# <span data-ttu-id="cc6db-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="cc6db-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="cc6db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc6db-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6db-103">Przywracanie serwera z istniejącej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="cc6db-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="cc6db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc6db-104">SYNTAX</span></span>

### <span data-ttu-id="cc6db-105">Subrestore (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cc6db-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cc6db-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="cc6db-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cc6db-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cc6db-107">DESCRIPTION</span></span>
<span data-ttu-id="cc6db-108">Przywracanie serwera z istniejącej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="cc6db-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="cc6db-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc6db-109">EXAMPLES</span></span>

### <span data-ttu-id="cc6db-110">Przykład 1: Przywracanie serwera MySql przy użyciu funkcji przywracania rerepliki</span><span class="sxs-lookup"><span data-stu-id="cc6db-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="cc6db-111">To polecenie cmdlet przywraca serwer MySql przy użyciu funkcji przywracania replik.</span><span class="sxs-lookup"><span data-stu-id="cc6db-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="cc6db-112">Przykład 2: Przywracanie serwera MySql przy użyciu funkcji przywracania PointInTime</span><span class="sxs-lookup"><span data-stu-id="cc6db-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="cc6db-113">Te polecenia cmdlet Przywróć serwer MySql przy użyciu funkcji przywracania PointInTime.</span><span class="sxs-lookup"><span data-stu-id="cc6db-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="cc6db-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc6db-114">PARAMETERS</span></span>

### <span data-ttu-id="cc6db-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc6db-115">-AsJob</span></span>
<span data-ttu-id="cc6db-116">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="cc6db-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="cc6db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6db-117">-DefaultProfile</span></span>
<span data-ttu-id="cc6db-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6db-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc6db-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc6db-119">-InputObject</span></span>
<span data-ttu-id="cc6db-120">Źródłowy obiekt serwera do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="cc6db-120">The source server object to restore from.</span></span>
<span data-ttu-id="cc6db-121">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="cc6db-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6db-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cc6db-122">-Location</span></span>
<span data-ttu-id="cc6db-123">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="cc6db-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="cc6db-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc6db-124">-Name</span></span>
<span data-ttu-id="cc6db-125">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="cc6db-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6db-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cc6db-126">-NoWait</span></span>
<span data-ttu-id="cc6db-127">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="cc6db-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="cc6db-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc6db-128">-ResourceGroupName</span></span>
<span data-ttu-id="cc6db-129">Nazwa grupy zasobów zawierającej dany zasób możesz uzyskać tę wartość z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="cc6db-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6db-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="cc6db-130">-RestorePointInTime</span></span>
<span data-ttu-id="cc6db-131">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="cc6db-131">The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6db-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="cc6db-132">-Sku</span></span>
<span data-ttu-id="cc6db-133">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cc6db-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="cc6db-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cc6db-134">-SubscriptionId</span></span>
<span data-ttu-id="cc6db-135">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6db-135">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6db-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc6db-136">-Tag</span></span>
<span data-ttu-id="cc6db-137">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="cc6db-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="cc6db-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="cc6db-138">-UseGeoRestore</span></span>
<span data-ttu-id="cc6db-139">Przywracanie za pomocą trybu geograficznego</span><span class="sxs-lookup"><span data-stu-id="cc6db-139">Use Geo mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6db-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="cc6db-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="cc6db-141">Przywracanie za pomocą trybu PointInTime</span><span class="sxs-lookup"><span data-stu-id="cc6db-141">Use PointInTime mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6db-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc6db-142">-Confirm</span></span>
<span data-ttu-id="cc6db-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc6db-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc6db-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc6db-144">-WhatIf</span></span>
<span data-ttu-id="cc6db-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc6db-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc6db-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc6db-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc6db-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6db-147">CommonParameters</span></span>
<span data-ttu-id="cc6db-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc6db-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6db-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc6db-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6db-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc6db-150">INPUTS</span></span>

### <span data-ttu-id="cc6db-151">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="cc6db-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="cc6db-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc6db-152">OUTPUTS</span></span>

### <span data-ttu-id="cc6db-153">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="cc6db-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="cc6db-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc6db-154">NOTES</span></span>

<span data-ttu-id="cc6db-155">PISUJE</span><span class="sxs-lookup"><span data-stu-id="cc6db-155">ALIASES</span></span>

<span data-ttu-id="cc6db-156">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc6db-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc6db-157">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cc6db-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc6db-158">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc6db-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc6db-159">WEJŚCIE <IServer> : obiekt serwera źródłowego do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="cc6db-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="cc6db-160">`Location <String>`: Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="cc6db-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="cc6db-161">`SkuName <String>`: Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cc6db-161">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="cc6db-162">`[Tag <ITrackedResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc6db-162">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="cc6db-163">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="cc6db-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cc6db-164">`[AdministratorLogin <String>]`: Nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="cc6db-164">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="cc6db-165">Można określić tylko podczas tworzenia serwera (i jest on wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="cc6db-165">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="cc6db-166">`[EarliestRestoreDate <DateTime?>]`: Najwcześniejszy czas tworzenia punktu przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="cc6db-166">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="cc6db-167">`[FullyQualifiedDomainName <String>]`: W pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="cc6db-167">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="cc6db-168">`[IdentityType <IdentityType?>]`: Typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="cc6db-168">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="cc6db-169">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać podmiot zabezpieczeń usługi Azure Active Directory dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="cc6db-169">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="cc6db-170">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stan wskazujący, czy na serwerze włączono szyfrowanie infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="cc6db-170">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="cc6db-171">`[MasterServerId <String>]`: Identyfikator głównego serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="cc6db-171">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="cc6db-172">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Wymuszanie minimalnej wersji protokołu TLS dla serwera.</span><span class="sxs-lookup"><span data-stu-id="cc6db-172">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="cc6db-173">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Określanie, czy dla tego serwera jest dozwolony dostęp do sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="cc6db-173">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="cc6db-174">Wartość jest opcjonalna, ale jeśli została przekazana, musi być "włączone" lub "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="cc6db-174">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="cc6db-175">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="cc6db-175">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="cc6db-176">`[ReplicationRole <String>]`: Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="cc6db-176">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="cc6db-177">`[SkuCapacity <Int32?>]`: Wydajność skalowania w górę/poza, reprezentująca jednostki obliczeniowe serwera.</span><span class="sxs-lookup"><span data-stu-id="cc6db-177">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="cc6db-178">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="cc6db-178">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="cc6db-179">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany według odpowiednich zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc6db-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="cc6db-180">`[SkuTier <SkuTier?>]`: Warstwa konkretnej jednostki SKU, na przykład podstawowa.</span><span class="sxs-lookup"><span data-stu-id="cc6db-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="cc6db-181">`[SslEnforcement <SslEnforcementEnum?>]`: Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="cc6db-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="cc6db-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej serwera.</span><span class="sxs-lookup"><span data-stu-id="cc6db-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="cc6db-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włączanie geograficznie nadmiarowych lub niezwiązanych z kopią zapasową serwera.</span><span class="sxs-lookup"><span data-stu-id="cc6db-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="cc6db-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włączanie automatycznego zwiększania przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="cc6db-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="cc6db-185">`[StorageProfileStorageMb <Int32?>]`: Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="cc6db-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="cc6db-186">`[UserVisibleState <ServerState?>]`: Stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cc6db-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="cc6db-187">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="cc6db-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="cc6db-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc6db-188">RELATED LINKS</span></span>

