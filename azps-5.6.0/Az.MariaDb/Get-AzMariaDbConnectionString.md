---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 6b0aad7829dc337869c26656135d039b5f74974f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983018"
---
# <span data-ttu-id="7a5c2-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="7a5c2-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="7a5c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5c2-103">Uzyskiwanie parametrów połączenia bazy danych MariaDB w ramach owej struktury.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="7a5c2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a5c2-104">SYNTAX</span></span>

### <span data-ttu-id="7a5c2-105">Nazwa_serwera (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7a5c2-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7a5c2-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="7a5c2-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a5c2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a5c2-107">DESCRIPTION</span></span>
<span data-ttu-id="7a5c2-108">Uzyskiwanie parametrów połączenia bazy danych MariaDB w ramach owej struktury.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="7a5c2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a5c2-109">EXAMPLES</span></span>

### <span data-ttu-id="7a5c2-110">Przykład 1. Uzyskiwanie parametrów połączenia z usługą MariaDB</span><span class="sxs-lookup"><span data-stu-id="7a5c2-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="7a5c2-111">To polecenie otrzymuje ciąg połączenia typu MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="7a5c2-112">Przykład 2. Uzyskiwanie parametrów połączenia z usługą MariaDB</span><span class="sxs-lookup"><span data-stu-id="7a5c2-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="7a5c2-113">To polecenie otrzymuje ciąg połączenia typu MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="7a5c2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a5c2-114">PARAMETERS</span></span>

### <span data-ttu-id="7a5c2-115">—Klient</span><span class="sxs-lookup"><span data-stu-id="7a5c2-115">-Client</span></span>
<span data-ttu-id="7a5c2-116">Typ klienta połączenia</span><span class="sxs-lookup"><span data-stu-id="7a5c2-116">Connect client type</span></span>

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

### <span data-ttu-id="7a5c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5c2-117">-DefaultProfile</span></span>
<span data-ttu-id="7a5c2-118">Region DefaultParameters Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a5c2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a5c2-119">-InputObject</span></span>
<span data-ttu-id="7a5c2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7a5c2-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7a5c2-121">-Name</span></span>
<span data-ttu-id="7a5c2-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-122">The name of the server.</span></span>

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

### <span data-ttu-id="7a5c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a5c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a5c2-124">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="7a5c2-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a5c2-125">-SubscriptionId</span></span>
<span data-ttu-id="7a5c2-126">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi</span><span class="sxs-lookup"><span data-stu-id="7a5c2-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="7a5c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5c2-127">CommonParameters</span></span>
<span data-ttu-id="7a5c2-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5c2-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a5c2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5c2-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a5c2-130">INPUTS</span></span>

### <span data-ttu-id="7a5c2-131">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="7a5c2-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="7a5c2-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a5c2-132">OUTPUTS</span></span>

### <span data-ttu-id="7a5c2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7a5c2-133">System.String</span></span>

## <span data-ttu-id="7a5c2-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a5c2-134">NOTES</span></span>

<span data-ttu-id="7a5c2-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7a5c2-135">ALIASES</span></span>

<span data-ttu-id="7a5c2-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a5c2-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a5c2-137">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a5c2-138">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a5c2-139">INPUTOBJECT: <IServer> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="7a5c2-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="7a5c2-140">`Location <String>`: lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="7a5c2-141">`[Tag <ITrackedResourceTags>]`: Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="7a5c2-142">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7a5c2-143">`[AdministratorLogin <String>]`: nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="7a5c2-144">Można określić tylko wtedy, gdy serwer jest tworzony (i jest wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="7a5c2-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="7a5c2-145">`[EarliestRestoreDate <DateTime?>]`: najwcześniejszy czas tworzenia punktów przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="7a5c2-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="7a5c2-146">`[FullyQualifiedDomainName <String>]`: w pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="7a5c2-147">`[IdentityType <IdentityType?>]`: typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="7a5c2-148">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać do zasobu podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="7a5c2-149">`[MasterServerId <String>]`: Główny identyfikator serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="7a5c2-150">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="7a5c2-151">`[ReplicationRole <String>]`: rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="7a5c2-152">`[SkuCapacity <Int32?>]`: Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="7a5c2-153">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="7a5c2-154">`[SkuName <String>]`: nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="7a5c2-155">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany przez zasób w zależności od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="7a5c2-156">`[SkuTier <SkuTier?>]`: warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="7a5c2-157">`[SslEnforcement <SslEnforcementEnum?>]`: Włącz wymuszanie ssl lub nie wymusz w przypadku łączenia się z serwerem.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="7a5c2-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="7a5c2-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włącz funkcję nadmiarowej lokalizacji geograficznej lub nie umożliwia tworzenia kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="7a5c2-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="7a5c2-161">`[StorageProfileStorageMb <Int32?>]`: Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="7a5c2-162">`[UserVisibleState <ServerState?>]`: stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="7a5c2-163">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="7a5c2-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a5c2-164">RELATED LINKS</span></span>

