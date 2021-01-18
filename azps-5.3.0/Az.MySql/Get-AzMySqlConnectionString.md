---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: d6dda5e26603c2276210e4bf00b8b9c040568f12
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499646"
---
# <span data-ttu-id="ac19e-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="ac19e-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="ac19e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac19e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac19e-103">Pobierz parametry połączenia w zależności od dostawcy połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="ac19e-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="ac19e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac19e-104">SYNTAX</span></span>

### <span data-ttu-id="ac19e-105">Get (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ac19e-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ac19e-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ac19e-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac19e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ac19e-107">DESCRIPTION</span></span>
<span data-ttu-id="ac19e-108">Pobierz parametry połączenia w zależności od dostawcy połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="ac19e-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="ac19e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac19e-109">EXAMPLES</span></span>

### <span data-ttu-id="ac19e-110">Przykład 1: pobieranie parametrów połączenia z serwerem MySql według grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="ac19e-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="ac19e-111">To polecenie cmdlet umożliwia pobieranie parametrów połączenia serwera MySql według grupy zasobów i nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="ac19e-112">Przykład 2: pobieranie parametrów połączenia z serwerem MySql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="ac19e-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="ac19e-113">To polecenie cmdlet umożliwia pobieranie parametrów połączenia serwera MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ac19e-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="ac19e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac19e-114">PARAMETERS</span></span>

### <span data-ttu-id="ac19e-115">-Client</span><span class="sxs-lookup"><span data-stu-id="ac19e-115">-Client</span></span>
<span data-ttu-id="ac19e-116">Dostawca połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="ac19e-116">Client connection provider.</span></span>

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

### <span data-ttu-id="ac19e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac19e-117">-DefaultProfile</span></span>
<span data-ttu-id="ac19e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac19e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac19e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ac19e-119">-InputObject</span></span>
<span data-ttu-id="ac19e-120">Obiekt serwera źródłowego, z którego ma zostać utworzona replika.</span><span class="sxs-lookup"><span data-stu-id="ac19e-120">The source server object to create replica from.</span></span>
<span data-ttu-id="ac19e-121">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="ac19e-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac19e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ac19e-122">-Name</span></span>
<span data-ttu-id="ac19e-123">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac19e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac19e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac19e-125">Nazwa grupy zasobów zawierającej dany zasób możesz uzyskać tę wartość z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ac19e-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac19e-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ac19e-126">-SubscriptionId</span></span>
<span data-ttu-id="ac19e-127">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ac19e-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac19e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac19e-128">CommonParameters</span></span>
<span data-ttu-id="ac19e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac19e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac19e-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac19e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac19e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac19e-131">INPUTS</span></span>

### <span data-ttu-id="ac19e-132">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="ac19e-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ac19e-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac19e-133">OUTPUTS</span></span>

### <span data-ttu-id="ac19e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ac19e-134">System.String</span></span>

## <span data-ttu-id="ac19e-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac19e-135">NOTES</span></span>

<span data-ttu-id="ac19e-136">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ac19e-136">ALIASES</span></span>

<span data-ttu-id="ac19e-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac19e-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac19e-138">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ac19e-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac19e-139">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac19e-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac19e-140">WEJŚCIE <IServer> : obiekt serwera źródłowego, z którego ma zostać utworzona replika.</span><span class="sxs-lookup"><span data-stu-id="ac19e-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="ac19e-141">`Location <String>`: Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="ac19e-141">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="ac19e-142">`SkuName <String>`: Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ac19e-142">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="ac19e-143">`[Tag <ITrackedResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="ac19e-143">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ac19e-144">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ac19e-144">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ac19e-145">`[AdministratorLogin <String>]`: Nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-145">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="ac19e-146">Można określić tylko podczas tworzenia serwera (i jest on wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="ac19e-146">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="ac19e-147">`[EarliestRestoreDate <DateTime?>]`: Najwcześniejszy czas tworzenia punktu przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="ac19e-147">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="ac19e-148">`[FullyQualifiedDomainName <String>]`: W pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-148">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="ac19e-149">`[IdentityType <IdentityType?>]`: Typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ac19e-149">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="ac19e-150">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać podmiot zabezpieczeń usługi Azure Active Directory dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="ac19e-150">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="ac19e-151">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stan wskazujący, czy na serwerze włączono szyfrowanie infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="ac19e-151">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="ac19e-152">`[MasterServerId <String>]`: Identyfikator głównego serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="ac19e-152">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="ac19e-153">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Wymuszanie minimalnej wersji protokołu TLS dla serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-153">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="ac19e-154">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Określanie, czy dla tego serwera jest dozwolony dostęp do sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="ac19e-154">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="ac19e-155">Wartość jest opcjonalna, ale jeśli została przekazana, musi być "włączone" lub "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="ac19e-155">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="ac19e-156">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="ac19e-156">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="ac19e-157">`[ReplicationRole <String>]`: Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-157">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="ac19e-158">`[SkuCapacity <Int32?>]`: Wydajność skalowania w górę/poza, reprezentująca jednostki obliczeniowe serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-158">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="ac19e-159">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="ac19e-159">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="ac19e-160">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany według odpowiednich zasobów.</span><span class="sxs-lookup"><span data-stu-id="ac19e-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="ac19e-161">`[SkuTier <SkuTier?>]`: Warstwa konkretnej jednostki SKU, na przykład podstawowa.</span><span class="sxs-lookup"><span data-stu-id="ac19e-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="ac19e-162">`[SslEnforcement <SslEnforcementEnum?>]`: Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="ac19e-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="ac19e-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="ac19e-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włączanie geograficznie nadmiarowych lub niezwiązanych z kopią zapasową serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="ac19e-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włączanie automatycznego zwiększania przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="ac19e-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="ac19e-166">`[StorageProfileStorageMb <Int32?>]`: Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="ac19e-167">`[UserVisibleState <ServerState?>]`: Stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ac19e-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="ac19e-168">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="ac19e-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="ac19e-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac19e-169">RELATED LINKS</span></span>

