---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 54463e38982a711f98515879f826a3cd2e068384
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498929"
---
# <span data-ttu-id="683ec-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="683ec-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="683ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="683ec-102">SYNOPSIS</span></span>
<span data-ttu-id="683ec-103">Tworzy nową replikę z istniejącej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="683ec-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="683ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="683ec-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="683ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="683ec-105">DESCRIPTION</span></span>
<span data-ttu-id="683ec-106">Tworzy nową replikę z istniejącej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="683ec-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="683ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="683ec-107">EXAMPLES</span></span>

### <span data-ttu-id="683ec-108">Przykład 1. Tworzenie nowej repliki serwera MySql</span><span class="sxs-lookup"><span data-stu-id="683ec-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="683ec-109">To polecenie cmdlet powoduje utworzenie nowej repliki serwera MySql.</span><span class="sxs-lookup"><span data-stu-id="683ec-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="683ec-110">Przykład 2: Tworzenie nowej repliki serwera MySql</span><span class="sxs-lookup"><span data-stu-id="683ec-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="683ec-111">To polecenie cmdlet z parametrem Master (inputobject) powoduje utworzenie nowej repliki serwera MySql.</span><span class="sxs-lookup"><span data-stu-id="683ec-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="683ec-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="683ec-112">PARAMETERS</span></span>

### <span data-ttu-id="683ec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="683ec-113">-AsJob</span></span>
<span data-ttu-id="683ec-114">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="683ec-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="683ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683ec-115">-DefaultProfile</span></span>
<span data-ttu-id="683ec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="683ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="683ec-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="683ec-117">-Location</span></span>
<span data-ttu-id="683ec-118">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="683ec-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="683ec-119">-Master</span><span class="sxs-lookup"><span data-stu-id="683ec-119">-Master</span></span>
<span data-ttu-id="683ec-120">Obiekt serwera źródłowego, z którego ma zostać utworzona replika.</span><span class="sxs-lookup"><span data-stu-id="683ec-120">The source server object to create replica from.</span></span>
<span data-ttu-id="683ec-121">Aby skonstruować, zobacz sekcję notatki dla właściwości wzorca i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="683ec-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="683ec-122">-Nowait</span><span class="sxs-lookup"><span data-stu-id="683ec-122">-NoWait</span></span>
<span data-ttu-id="683ec-123">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="683ec-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="683ec-124">-Replica</span><span class="sxs-lookup"><span data-stu-id="683ec-124">-Replica</span></span>
<span data-ttu-id="683ec-125">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="683ec-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="683ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="683ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="683ec-127">Nazwa grupy zasobów zawierającej dany zasób możesz uzyskać tę wartość z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="683ec-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="683ec-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="683ec-128">-Sku</span></span>
<span data-ttu-id="683ec-129">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="683ec-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="683ec-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="683ec-130">-SubscriptionId</span></span>
<span data-ttu-id="683ec-131">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="683ec-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="683ec-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="683ec-132">-Confirm</span></span>
<span data-ttu-id="683ec-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="683ec-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="683ec-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="683ec-134">-WhatIf</span></span>
<span data-ttu-id="683ec-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="683ec-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="683ec-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="683ec-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="683ec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683ec-137">CommonParameters</span></span>
<span data-ttu-id="683ec-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="683ec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683ec-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="683ec-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683ec-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="683ec-140">INPUTS</span></span>

### <span data-ttu-id="683ec-141">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="683ec-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="683ec-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="683ec-142">OUTPUTS</span></span>

### <span data-ttu-id="683ec-143">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="683ec-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="683ec-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="683ec-144">NOTES</span></span>

<span data-ttu-id="683ec-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="683ec-145">ALIASES</span></span>

<span data-ttu-id="683ec-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="683ec-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="683ec-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="683ec-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="683ec-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="683ec-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="683ec-149">WZORZEC <IServer> : obiekt serwera źródłowego, z którego ma zostać utworzona replika.</span><span class="sxs-lookup"><span data-stu-id="683ec-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="683ec-150">`Location <String>`: Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="683ec-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="683ec-151">`SkuName <String>`: Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="683ec-151">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="683ec-152">`[Tag <ITrackedResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="683ec-152">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="683ec-153">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="683ec-153">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="683ec-154">`[AdministratorLogin <String>]`: Nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="683ec-154">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="683ec-155">Można określić tylko podczas tworzenia serwera (i jest on wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="683ec-155">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="683ec-156">`[EarliestRestoreDate <DateTime?>]`: Najwcześniejszy czas tworzenia punktu przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="683ec-156">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="683ec-157">`[FullyQualifiedDomainName <String>]`: W pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="683ec-157">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="683ec-158">`[IdentityType <IdentityType?>]`: Typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="683ec-158">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="683ec-159">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać podmiot zabezpieczeń usługi Azure Active Directory dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="683ec-159">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="683ec-160">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stan wskazujący, czy na serwerze włączono szyfrowanie infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="683ec-160">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="683ec-161">`[MasterServerId <String>]`: Identyfikator głównego serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="683ec-161">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="683ec-162">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Wymuszanie minimalnej wersji protokołu TLS dla serwera.</span><span class="sxs-lookup"><span data-stu-id="683ec-162">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="683ec-163">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Określanie, czy dla tego serwera jest dozwolony dostęp do sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="683ec-163">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="683ec-164">Wartość jest opcjonalna, ale jeśli została przekazana, musi być "włączone" lub "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="683ec-164">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="683ec-165">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="683ec-165">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="683ec-166">`[ReplicationRole <String>]`: Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="683ec-166">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="683ec-167">`[SkuCapacity <Int32?>]`: Wydajność skalowania w górę/poza, reprezentująca jednostki obliczeniowe serwera.</span><span class="sxs-lookup"><span data-stu-id="683ec-167">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="683ec-168">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="683ec-168">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="683ec-169">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany według odpowiednich zasobów.</span><span class="sxs-lookup"><span data-stu-id="683ec-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="683ec-170">`[SkuTier <SkuTier?>]`: Warstwa konkretnej jednostki SKU, na przykład podstawowa.</span><span class="sxs-lookup"><span data-stu-id="683ec-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="683ec-171">`[SslEnforcement <SslEnforcementEnum?>]`: Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="683ec-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="683ec-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej serwera.</span><span class="sxs-lookup"><span data-stu-id="683ec-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="683ec-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włączanie geograficznie nadmiarowych lub niezwiązanych z kopią zapasową serwera.</span><span class="sxs-lookup"><span data-stu-id="683ec-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="683ec-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włączanie automatycznego zwiększania przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="683ec-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="683ec-175">`[StorageProfileStorageMb <Int32?>]`: Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="683ec-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="683ec-176">`[UserVisibleState <ServerState?>]`: Stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="683ec-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="683ec-177">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="683ec-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="683ec-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="683ec-178">RELATED LINKS</span></span>

