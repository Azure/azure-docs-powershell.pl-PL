---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190266"
---
# <span data-ttu-id="ce7f0-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="ce7f0-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="ce7f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7f0-103">Uzyskiwanie parametrów połączenia bazy danych MariaDB w ramach owej struktury.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="ce7f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ce7f0-104">SYNTAX</span></span>

### <span data-ttu-id="ce7f0-105">Nazwa_serwera (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ce7f0-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ce7f0-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="ce7f0-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce7f0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ce7f0-107">DESCRIPTION</span></span>
<span data-ttu-id="ce7f0-108">Uzyskiwanie parametrów połączenia bazy danych MariaDB w ramach owej struktury.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="ce7f0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ce7f0-109">EXAMPLES</span></span>

### <span data-ttu-id="ce7f0-110">Przykład 1. Uzyskiwanie parametrów połączenia z usługą MariaDB</span><span class="sxs-lookup"><span data-stu-id="ce7f0-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="ce7f0-111">To polecenie otrzymuje ciąg połączenia typu MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="ce7f0-112">Przykład 2. Uzyskiwanie parametrów połączenia z usługą MariaDB</span><span class="sxs-lookup"><span data-stu-id="ce7f0-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="ce7f0-113">To polecenie otrzymuje ciąg połączenia typu MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="ce7f0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce7f0-114">PARAMETERS</span></span>

### <span data-ttu-id="ce7f0-115">—Klient</span><span class="sxs-lookup"><span data-stu-id="ce7f0-115">-Client</span></span>
<span data-ttu-id="ce7f0-116">Typ klienta połączenia</span><span class="sxs-lookup"><span data-stu-id="ce7f0-116">Connect client type</span></span>

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

### <span data-ttu-id="ce7f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce7f0-117">-DefaultProfile</span></span>
<span data-ttu-id="ce7f0-118">Region DefaultParameters Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce7f0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce7f0-119">-InputObject</span></span>
<span data-ttu-id="ce7f0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ce7f0-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ce7f0-121">-Name</span></span>
<span data-ttu-id="ce7f0-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-122">The name of the server.</span></span>

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

### <span data-ttu-id="ce7f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce7f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="ce7f0-124">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="ce7f0-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce7f0-125">-SubscriptionId</span></span>
<span data-ttu-id="ce7f0-126">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi</span><span class="sxs-lookup"><span data-stu-id="ce7f0-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="ce7f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7f0-127">CommonParameters</span></span>
<span data-ttu-id="ce7f0-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7f0-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce7f0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7f0-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce7f0-130">INPUTS</span></span>

### <span data-ttu-id="ce7f0-131">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="ce7f0-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="ce7f0-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce7f0-132">OUTPUTS</span></span>

### <span data-ttu-id="ce7f0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ce7f0-133">System.String</span></span>

## <span data-ttu-id="ce7f0-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ce7f0-134">NOTES</span></span>

<span data-ttu-id="ce7f0-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ce7f0-135">ALIASES</span></span>

<span data-ttu-id="ce7f0-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce7f0-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce7f0-137">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce7f0-138">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce7f0-139">INPUTOBJECT: <IServer> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ce7f0-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="ce7f0-140">`Location <String>`: lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="ce7f0-141">`[Tag <ITrackedResourceTags>]`: Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="ce7f0-142">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ce7f0-143">`[AdministratorLogin <String>]`: nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="ce7f0-144">Można określić tylko wtedy, gdy serwer jest tworzony (i jest wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="ce7f0-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="ce7f0-145">`[EarliestRestoreDate <DateTime?>]`: najwcześniejszy czas tworzenia punktów przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="ce7f0-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="ce7f0-146">`[FullyQualifiedDomainName <String>]`: w pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="ce7f0-147">`[IdentityType <IdentityType?>]`: typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="ce7f0-148">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać do zasobu podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="ce7f0-149">`[MasterServerId <String>]`: Główny identyfikator serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="ce7f0-150">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="ce7f0-151">`[ReplicationRole <String>]`: Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="ce7f0-152">`[SkuCapacity <Int32?>]`: Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="ce7f0-153">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="ce7f0-154">`[SkuName <String>]`: nazwa sKU, zazwyczaj warstwa + rodzina + podstawy, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="ce7f0-155">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany przez zasób w zależności od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="ce7f0-156">`[SkuTier <SkuTier?>]`: warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="ce7f0-157">`[SslEnforcement <SslEnforcementEnum?>]`: Włącz wymuszanie ssl lub nie wymusz w przypadku łączenia się z serwerem.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="ce7f0-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="ce7f0-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włącz funkcję nadmiarowej lokalizacji geograficznej lub nie umożliwia tworzenia kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="ce7f0-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="ce7f0-161">`[StorageProfileStorageMb <Int32?>]`: Maksymalna dozwolona ilość miejsca do magazynowania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="ce7f0-162">`[UserVisibleState <ServerState?>]`: stan serwera widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="ce7f0-163">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="ce7f0-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce7f0-164">RELATED LINKS</span></span>

