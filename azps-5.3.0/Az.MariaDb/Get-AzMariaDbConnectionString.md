---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380732"
---
# <span data-ttu-id="d9b75-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="d9b75-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="d9b75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9b75-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b75-103">Pobierz parametry połączenia MariaDB w ramach danej struktury.</span><span class="sxs-lookup"><span data-stu-id="d9b75-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="d9b75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9b75-104">SYNTAX</span></span>

### <span data-ttu-id="d9b75-105">Nazwa_serwera (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d9b75-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9b75-106">Serverobject</span><span class="sxs-lookup"><span data-stu-id="d9b75-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9b75-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d9b75-107">DESCRIPTION</span></span>
<span data-ttu-id="d9b75-108">Pobierz parametry połączenia MariaDB w ramach danej struktury.</span><span class="sxs-lookup"><span data-stu-id="d9b75-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="d9b75-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9b75-109">EXAMPLES</span></span>

### <span data-ttu-id="d9b75-110">Przykład 1. pobieranie parametrów połączenia z MariaDB</span><span class="sxs-lookup"><span data-stu-id="d9b75-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="d9b75-111">To polecenie pobiera parametry połączenia z MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d9b75-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="d9b75-112">Przykład 2: pobieranie parametrów połączenia z MariaDB</span><span class="sxs-lookup"><span data-stu-id="d9b75-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="d9b75-113">To polecenie pobiera parametry połączenia z MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d9b75-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="d9b75-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9b75-114">PARAMETERS</span></span>

### <span data-ttu-id="d9b75-115">-Client</span><span class="sxs-lookup"><span data-stu-id="d9b75-115">-Client</span></span>
<span data-ttu-id="d9b75-116">Typ klienta połączenia</span><span class="sxs-lookup"><span data-stu-id="d9b75-116">Connect client type</span></span>

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

### <span data-ttu-id="d9b75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b75-117">-DefaultProfile</span></span>
<span data-ttu-id="d9b75-118">Region DefaultParameters poświadczenia, konto, dzierżawca i abonament używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b75-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9b75-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d9b75-119">-InputObject</span></span>
<span data-ttu-id="d9b75-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d9b75-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b75-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9b75-121">-Name</span></span>
<span data-ttu-id="d9b75-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="d9b75-122">The name of the server.</span></span>

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

### <span data-ttu-id="d9b75-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b75-123">-ResourceGroupName</span></span>
<span data-ttu-id="d9b75-124">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="d9b75-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="d9b75-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d9b75-125">-SubscriptionId</span></span>
<span data-ttu-id="d9b75-126">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą</span><span class="sxs-lookup"><span data-stu-id="d9b75-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="d9b75-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b75-127">CommonParameters</span></span>
<span data-ttu-id="d9b75-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b75-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b75-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9b75-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b75-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9b75-130">INPUTS</span></span>

### <span data-ttu-id="d9b75-131">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="d9b75-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="d9b75-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9b75-132">OUTPUTS</span></span>

### <span data-ttu-id="d9b75-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d9b75-133">System.String</span></span>

## <span data-ttu-id="d9b75-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9b75-134">NOTES</span></span>

<span data-ttu-id="d9b75-135">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d9b75-135">ALIASES</span></span>

<span data-ttu-id="d9b75-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9b75-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d9b75-137">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d9b75-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9b75-138">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9b75-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d9b75-139">INPUTobject <IServer> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d9b75-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="d9b75-140">`Location <String>`: Lokalizacja, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="d9b75-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="d9b75-141">`[Tag <ITrackedResourceTags>]`: Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="d9b75-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="d9b75-142">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="d9b75-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d9b75-143">`[AdministratorLogin <String>]`: Nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="d9b75-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="d9b75-144">Można określić tylko podczas tworzenia serwera (i jest on wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="d9b75-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="d9b75-145">`[EarliestRestoreDate <DateTime?>]`: Najwcześniejszy czas tworzenia punktu przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="d9b75-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="d9b75-146">`[FullyQualifiedDomainName <String>]`: W pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="d9b75-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="d9b75-147">`[IdentityType <IdentityType?>]`: Typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="d9b75-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="d9b75-148">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać podmiot zabezpieczeń usługi Azure Active Directory dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="d9b75-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="d9b75-149">`[MasterServerId <String>]`: Identyfikator głównego serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="d9b75-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="d9b75-150">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="d9b75-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="d9b75-151">`[ReplicationRole <String>]`: Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="d9b75-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="d9b75-152">`[SkuCapacity <Int32?>]`: Wydajność skalowania w górę/poza, reprezentująca jednostki obliczeniowe serwera.</span><span class="sxs-lookup"><span data-stu-id="d9b75-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="d9b75-153">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="d9b75-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="d9b75-154">`[SkuName <String>]`: Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="d9b75-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="d9b75-155">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany według odpowiednich zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9b75-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="d9b75-156">`[SkuTier <SkuTier?>]`: Warstwa konkretnej jednostki SKU, na przykład podstawowa.</span><span class="sxs-lookup"><span data-stu-id="d9b75-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="d9b75-157">`[SslEnforcement <SslEnforcementEnum?>]`: Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="d9b75-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="d9b75-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej serwera.</span><span class="sxs-lookup"><span data-stu-id="d9b75-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="d9b75-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włączanie geograficznie nadmiarowych lub niezwiązanych z kopią zapasową serwera.</span><span class="sxs-lookup"><span data-stu-id="d9b75-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="d9b75-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włączanie automatycznego zwiększania przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="d9b75-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="d9b75-161">`[StorageProfileStorageMb <Int32?>]`: Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="d9b75-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="d9b75-162">`[UserVisibleState <ServerState?>]`: Stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d9b75-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="d9b75-163">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="d9b75-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="d9b75-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9b75-164">RELATED LINKS</span></span>

