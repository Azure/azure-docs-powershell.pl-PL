---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
ms.openlocfilehash: 7eb1105985202bd8cd05a1b2f2e546e4dd834e50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179082"
---
# <span data-ttu-id="8d970-101">Restore-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="8d970-101">Restore-AzPostgreSqlServer</span></span>

## <span data-ttu-id="8d970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d970-102">SYNOPSIS</span></span>
<span data-ttu-id="8d970-103">Przywracanie serwera z istniejącej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="8d970-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="8d970-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8d970-104">SYNTAX</span></span>

### <span data-ttu-id="8d970-105">GeoRestore (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8d970-105">GeoRestore (Default)</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d970-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="8d970-106">PointInTimeRestore</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8d970-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8d970-107">DESCRIPTION</span></span>
<span data-ttu-id="8d970-108">Przywracanie serwera z istniejącej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="8d970-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="8d970-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8d970-109">EXAMPLES</span></span>

### <span data-ttu-id="8d970-110">Przykład 1. Przywracanie serwera PostgreSql przy użyciu funkcji Przywracania georeplicy</span><span class="sxs-lookup"><span data-stu-id="8d970-110">Example 1: Restore PostgreSql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName postgresqltestserverreplica | Restore-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -UseGeoRestore

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="8d970-111">To polecenie cmdlet przywraca serwer PostgreSql przy użyciu funkcji Przywracania georeplicy.</span><span class="sxs-lookup"><span data-stu-id="8d970-111">This cmdlet restores PostgreSql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="8d970-112">Przykład 2. Przywracanie serwera PostgreSql przy użyciu funkcji Przywracania punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="8d970-112">Example 2: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Restore-AzPostgreSqlServer -Name PostgreSqlTestServerGEO -ResourceGroupName PostgreSqlTestRG -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name                    Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                    -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestservergeo eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="8d970-113">Te polecenia cmdlet przywróć serwer PostgreSql przy użyciu funkcji przywracania PointInTime.</span><span class="sxs-lookup"><span data-stu-id="8d970-113">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="8d970-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d970-114">PARAMETERS</span></span>

### <span data-ttu-id="8d970-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8d970-115">-AsJob</span></span>
<span data-ttu-id="8d970-116">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="8d970-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="8d970-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d970-117">-DefaultProfile</span></span>
<span data-ttu-id="8d970-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d970-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d970-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d970-119">-InputObject</span></span>
<span data-ttu-id="8d970-120">Obiekt serwera źródłowego, z którym chcesz przywrócić dane.</span><span class="sxs-lookup"><span data-stu-id="8d970-120">The source server object to restore from.</span></span>
<span data-ttu-id="8d970-121">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="8d970-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d970-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8d970-122">-Location</span></span>
<span data-ttu-id="8d970-123">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="8d970-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="8d970-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8d970-124">-Name</span></span>
<span data-ttu-id="8d970-125">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="8d970-125">The name of the server.</span></span>

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

### <span data-ttu-id="8d970-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8d970-126">-NoWait</span></span>
<span data-ttu-id="8d970-127">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="8d970-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8d970-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d970-128">-ResourceGroupName</span></span>
<span data-ttu-id="8d970-129">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="8d970-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8d970-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="8d970-130">-RestorePointInTime</span></span>
<span data-ttu-id="8d970-131">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="8d970-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="8d970-132">- SKU</span><span class="sxs-lookup"><span data-stu-id="8d970-132">-Sku</span></span>
<span data-ttu-id="8d970-133">Nazwa sKU, zwykle warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8d970-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="8d970-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d970-134">-SubscriptionId</span></span>
<span data-ttu-id="8d970-135">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8d970-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8d970-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="8d970-136">-Tag</span></span>
<span data-ttu-id="8d970-137">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="8d970-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8d970-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="8d970-138">-UseGeoRestore</span></span>
<span data-ttu-id="8d970-139">Przywracanie za pomocą trybu geolokalizacji</span><span class="sxs-lookup"><span data-stu-id="8d970-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="8d970-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="8d970-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="8d970-141">Przywracanie za pomocą trybu PointInTime</span><span class="sxs-lookup"><span data-stu-id="8d970-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="8d970-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d970-142">-Confirm</span></span>
<span data-ttu-id="8d970-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8d970-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d970-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d970-144">-WhatIf</span></span>
<span data-ttu-id="8d970-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d970-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d970-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8d970-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d970-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d970-147">CommonParameters</span></span>
<span data-ttu-id="8d970-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d970-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d970-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d970-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d970-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d970-150">INPUTS</span></span>

### <span data-ttu-id="8d970-151">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="8d970-151">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8d970-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d970-152">OUTPUTS</span></span>

### <span data-ttu-id="8d970-153">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="8d970-153">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8d970-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8d970-154">NOTES</span></span>

<span data-ttu-id="8d970-155">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8d970-155">ALIASES</span></span>

<span data-ttu-id="8d970-156">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="8d970-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d970-157">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8d970-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d970-158">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d970-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d970-159">INPUTOBJECT: <IServer> obiekt serwera źródłowego, z którym należy przywrócić dane.</span><span class="sxs-lookup"><span data-stu-id="8d970-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="8d970-160">`Location <String>`: lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="8d970-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="8d970-161">`[Tag <ITrackedResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d970-161">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="8d970-162">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="8d970-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8d970-163">`[AdministratorLogin <String>]`: nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="8d970-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="8d970-164">Można określić tylko wtedy, gdy serwer jest tworzony (i jest wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="8d970-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="8d970-165">`[EarliestRestoreDate <DateTime?>]`: najwcześniejszy czas tworzenia punktów przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="8d970-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="8d970-166">`[FullyQualifiedDomainName <String>]`: w pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="8d970-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="8d970-167">`[IdentityType <IdentityType?>]`: typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="8d970-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="8d970-168">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać do zasobu podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d970-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="8d970-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stan pokazujący, czy szyfrowanie infrastruktury było włączone dla serwera.</span><span class="sxs-lookup"><span data-stu-id="8d970-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="8d970-170">`[MasterServerId <String>]`: Główny identyfikator serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="8d970-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="8d970-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: wymuszanie minimalnej wersji Tls dla serwera.</span><span class="sxs-lookup"><span data-stu-id="8d970-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="8d970-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: czy dla tego serwera jest dozwolony dostęp do sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="8d970-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="8d970-173">Wartość jest opcjonalna, ale jeśli zostanie przekazana, musi mieć wartość "Włączone" lub "Wyłączone".</span><span class="sxs-lookup"><span data-stu-id="8d970-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="8d970-174">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="8d970-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="8d970-175">`[ReplicationRole <String>]`: rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="8d970-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="8d970-176">`[SkuCapacity <Int32?>]`: Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.</span><span class="sxs-lookup"><span data-stu-id="8d970-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="8d970-177">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="8d970-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="8d970-178">`[SkuName <String>]`: nazwa sKU, zazwyczaj warstwa + rodzina + podstawy, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8d970-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="8d970-179">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany przez zasób w zależności od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="8d970-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="8d970-180">`[SkuTier <SkuTier?>]`: warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="8d970-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="8d970-181">`[SslEnforcement <SslEnforcementEnum?>]`: Włącz wymuszanie ssl lub nie wymusz w przypadku łączenia się z serwerem.</span><span class="sxs-lookup"><span data-stu-id="8d970-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="8d970-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="8d970-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="8d970-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włącz funkcję nadmiarowej lokalizacji geograficznej lub nie umożliwia tworzenia kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8d970-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="8d970-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="8d970-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="8d970-185">`[StorageProfileStorageMb <Int32?>]`: Maksymalna dozwolona ilość miejsca do magazynowania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8d970-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="8d970-186">`[UserVisibleState <ServerState?>]`: stan serwera widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8d970-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="8d970-187">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="8d970-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="8d970-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d970-188">RELATED LINKS</span></span>

