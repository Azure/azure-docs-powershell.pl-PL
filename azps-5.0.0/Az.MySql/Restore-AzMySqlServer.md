---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 49ae121273b42d3718d1a334edcaa72fa2c57583
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225543"
---
# <span data-ttu-id="ade04-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="ade04-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="ade04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ade04-102">SYNOPSIS</span></span>
<span data-ttu-id="ade04-103">Przywracanie serwera z istniejącej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="ade04-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="ade04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ade04-104">SYNTAX</span></span>

### <span data-ttu-id="ade04-105">Subrestore (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ade04-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ade04-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="ade04-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ade04-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ade04-107">DESCRIPTION</span></span>
<span data-ttu-id="ade04-108">Przywracanie serwera z istniejącej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="ade04-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="ade04-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ade04-109">EXAMPLES</span></span>

### <span data-ttu-id="ade04-110">Przykład 1: Przywracanie serwera MySql przy użyciu funkcji przywracania rerepliki</span><span class="sxs-lookup"><span data-stu-id="ade04-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="ade04-111">To polecenie cmdlet przywraca serwer MySql przy użyciu funkcji przywracania replik.</span><span class="sxs-lookup"><span data-stu-id="ade04-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="ade04-112">Przykład 2: Przywracanie serwera MySql przy użyciu funkcji przywracania PointInTime</span><span class="sxs-lookup"><span data-stu-id="ade04-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="ade04-113">Te polecenia cmdlet Przywróć serwer MySql przy użyciu funkcji przywracania PointInTime.</span><span class="sxs-lookup"><span data-stu-id="ade04-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="ade04-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ade04-114">PARAMETERS</span></span>

### <span data-ttu-id="ade04-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ade04-115">-AsJob</span></span>
<span data-ttu-id="ade04-116">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="ade04-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="ade04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade04-117">-DefaultProfile</span></span>
<span data-ttu-id="ade04-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ade04-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ade04-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ade04-119">-InputObject</span></span>
<span data-ttu-id="ade04-120">Źródłowy obiekt serwera do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="ade04-120">The source server object to restore from.</span></span>
<span data-ttu-id="ade04-121">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="ade04-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ade04-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ade04-122">-Location</span></span>
<span data-ttu-id="ade04-123">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="ade04-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ade04-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ade04-124">-Name</span></span>
<span data-ttu-id="ade04-125">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ade04-125">The name of the server.</span></span>

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

### <span data-ttu-id="ade04-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ade04-126">-NoWait</span></span>
<span data-ttu-id="ade04-127">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="ade04-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ade04-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade04-128">-ResourceGroupName</span></span>
<span data-ttu-id="ade04-129">Nazwa grupy zasobów zawierającej dany zasób możesz uzyskać tę wartość z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ade04-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ade04-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="ade04-130">-RestorePointInTime</span></span>
<span data-ttu-id="ade04-131">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="ade04-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ade04-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="ade04-132">-Sku</span></span>
<span data-ttu-id="ade04-133">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ade04-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="ade04-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ade04-134">-SubscriptionId</span></span>
<span data-ttu-id="ade04-135">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ade04-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ade04-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="ade04-136">-Tag</span></span>
<span data-ttu-id="ade04-137">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="ade04-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="ade04-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="ade04-138">-UseGeoRestore</span></span>
<span data-ttu-id="ade04-139">Przywracanie za pomocą trybu geograficznego</span><span class="sxs-lookup"><span data-stu-id="ade04-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="ade04-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="ade04-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="ade04-141">Przywracanie za pomocą trybu PointInTime</span><span class="sxs-lookup"><span data-stu-id="ade04-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="ade04-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ade04-142">-Confirm</span></span>
<span data-ttu-id="ade04-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade04-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade04-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade04-144">-WhatIf</span></span>
<span data-ttu-id="ade04-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade04-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade04-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ade04-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade04-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade04-147">CommonParameters</span></span>
<span data-ttu-id="ade04-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade04-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade04-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ade04-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade04-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ade04-150">INPUTS</span></span>

### <span data-ttu-id="ade04-151">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="ade04-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ade04-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ade04-152">OUTPUTS</span></span>

### <span data-ttu-id="ade04-153">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="ade04-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ade04-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ade04-154">NOTES</span></span>

<span data-ttu-id="ade04-155">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ade04-155">ALIASES</span></span>

<span data-ttu-id="ade04-156">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ade04-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ade04-157">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ade04-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ade04-158">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ade04-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ade04-159">WEJŚCIE <IServer> : obiekt serwera źródłowego do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="ade04-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="ade04-160">`Location <String>`: Lokalizacja, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="ade04-160">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="ade04-161">`[Tag <ITrackedResourceTags>]`: Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="ade04-161">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="ade04-162">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ade04-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ade04-163">`[AdministratorLogin <String>]`: Nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="ade04-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="ade04-164">Można określić tylko podczas tworzenia serwera (i jest on wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="ade04-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="ade04-165">`[EarliestRestoreDate <DateTime?>]`: Najwcześniejszy czas tworzenia punktu przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="ade04-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="ade04-166">`[FullyQualifiedDomainName <String>]`: W pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="ade04-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="ade04-167">`[IdentityType <IdentityType?>]`: Typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ade04-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="ade04-168">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać podmiot zabezpieczeń usługi Azure Active Directory dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="ade04-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="ade04-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stan wskazujący, czy na serwerze włączono szyfrowanie infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="ade04-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="ade04-170">`[MasterServerId <String>]`: Identyfikator głównego serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="ade04-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="ade04-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Wymuszanie minimalnej wersji protokołu TLS dla serwera.</span><span class="sxs-lookup"><span data-stu-id="ade04-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="ade04-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Określanie, czy dla tego serwera jest dozwolony dostęp do sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="ade04-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="ade04-173">Wartość jest opcjonalna, ale jeśli została przekazana, musi być "włączone" lub "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="ade04-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="ade04-174">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="ade04-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="ade04-175">`[ReplicationRole <String>]`: Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="ade04-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="ade04-176">`[SkuCapacity <Int32?>]`: Wydajność skalowania w górę/poza, reprezentująca jednostki obliczeniowe serwera.</span><span class="sxs-lookup"><span data-stu-id="ade04-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="ade04-177">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="ade04-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="ade04-178">`[SkuName <String>]`: Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ade04-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="ade04-179">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany według odpowiednich zasobów.</span><span class="sxs-lookup"><span data-stu-id="ade04-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="ade04-180">`[SkuTier <SkuTier?>]`: Warstwa konkretnej jednostki SKU, na przykład podstawowa.</span><span class="sxs-lookup"><span data-stu-id="ade04-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="ade04-181">`[SslEnforcement <SslEnforcementEnum?>]`: Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="ade04-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="ade04-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej serwera.</span><span class="sxs-lookup"><span data-stu-id="ade04-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="ade04-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włączanie geograficznie nadmiarowych lub niezwiązanych z kopią zapasową serwera.</span><span class="sxs-lookup"><span data-stu-id="ade04-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="ade04-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włączanie automatycznego zwiększania przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="ade04-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="ade04-185">`[StorageProfileStorageMb <Int32?>]`: Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="ade04-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="ade04-186">`[UserVisibleState <ServerState?>]`: Stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ade04-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="ade04-187">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="ade04-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="ade04-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ade04-188">RELATED LINKS</span></span>

