---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: ae0a5f2130ea4b5120fdbe78ab4cc23a7eba29a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996094"
---
# <span data-ttu-id="ff388-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="ff388-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="ff388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff388-102">SYNOPSIS</span></span>
<span data-ttu-id="ff388-103">Pobierz parametrów połączenia według dostawcy połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="ff388-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="ff388-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff388-104">SYNTAX</span></span>

### <span data-ttu-id="ff388-105">Pobierz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ff388-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff388-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ff388-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff388-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff388-107">DESCRIPTION</span></span>
<span data-ttu-id="ff388-108">Pobierz parametrów połączenia według dostawcy połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="ff388-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="ff388-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff388-109">EXAMPLES</span></span>

### <span data-ttu-id="ff388-110">Przykład 1. Uzyskiwanie parametrów połączenia serwera PostgreSql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="ff388-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="ff388-111">To polecenie cmdlet pobiera ciąg połączenia serwera PostgreSql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="ff388-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="ff388-112">Przykład 2. Uzyskiwanie parametrów połączenia serwera PostgreSql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="ff388-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="ff388-113">To polecenie cmdlet pobiera ciąg połączenia serwera PostgreSql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ff388-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="ff388-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff388-114">PARAMETERS</span></span>

### <span data-ttu-id="ff388-115">—Klient</span><span class="sxs-lookup"><span data-stu-id="ff388-115">-Client</span></span>
<span data-ttu-id="ff388-116">Dostawca połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="ff388-116">Client connection provider.</span></span>

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

### <span data-ttu-id="ff388-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff388-117">-DefaultProfile</span></span>
<span data-ttu-id="ff388-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff388-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff388-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff388-119">-InputObject</span></span>
<span data-ttu-id="ff388-120">Serwer parametrów połączenia Do skonstruowania, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="ff388-120">The server for the connection string To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff388-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ff388-121">-Name</span></span>
<span data-ttu-id="ff388-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ff388-122">The name of the server.</span></span>

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

### <span data-ttu-id="ff388-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff388-123">-ResourceGroupName</span></span>
<span data-ttu-id="ff388-124">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ff388-124">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ff388-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff388-125">-SubscriptionId</span></span>
<span data-ttu-id="ff388-126">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff388-126">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ff388-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff388-127">CommonParameters</span></span>
<span data-ttu-id="ff388-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff388-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff388-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff388-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff388-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff388-130">INPUTS</span></span>

### <span data-ttu-id="ff388-131">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="ff388-131">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ff388-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff388-132">OUTPUTS</span></span>

### <span data-ttu-id="ff388-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ff388-133">System.String</span></span>

## <span data-ttu-id="ff388-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff388-134">NOTES</span></span>

<span data-ttu-id="ff388-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ff388-135">ALIASES</span></span>

<span data-ttu-id="ff388-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff388-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff388-137">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ff388-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff388-138">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff388-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff388-139">INPUTOBJECT: <IServer> serwer parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="ff388-139">INPUTOBJECT <IServer>: The server for the connection string</span></span>
  - <span data-ttu-id="ff388-140">`Location <String>`: lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="ff388-140">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="ff388-141">`[Tag <ITrackedResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff388-141">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ff388-142">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ff388-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ff388-143">`[AdministratorLogin <String>]`: nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="ff388-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="ff388-144">Można określić tylko wtedy, gdy serwer jest tworzony (i jest wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="ff388-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="ff388-145">`[EarliestRestoreDate <DateTime?>]`: najwcześniejszy czas tworzenia punktów przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="ff388-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="ff388-146">`[FullyQualifiedDomainName <String>]`: w pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="ff388-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="ff388-147">`[IdentityType <IdentityType?>]`: typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ff388-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="ff388-148">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać do zasobu podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ff388-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="ff388-149">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stan pokazujący, czy szyfrowanie infrastruktury było włączone dla serwera.</span><span class="sxs-lookup"><span data-stu-id="ff388-149">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="ff388-150">`[MasterServerId <String>]`: Główny identyfikator serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="ff388-150">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="ff388-151">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: wymuszanie minimalnej wersji Tls dla serwera.</span><span class="sxs-lookup"><span data-stu-id="ff388-151">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="ff388-152">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: czy na tym serwerze jest dozwolony dostęp do sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="ff388-152">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="ff388-153">Wartość jest opcjonalna, ale jeśli zostanie przekazana, musi mieć wartość "Włączona" lub "Wyłączona".</span><span class="sxs-lookup"><span data-stu-id="ff388-153">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="ff388-154">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="ff388-154">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="ff388-155">`[ReplicationRole <String>]`: rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="ff388-155">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="ff388-156">`[SkuCapacity <Int32?>]`: Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.</span><span class="sxs-lookup"><span data-stu-id="ff388-156">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="ff388-157">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="ff388-157">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="ff388-158">`[SkuName <String>]`: nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ff388-158">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="ff388-159">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany przez zasób w zależności od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="ff388-159">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="ff388-160">`[SkuTier <SkuTier?>]`: warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="ff388-160">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="ff388-161">`[SslEnforcement <SslEnforcementEnum?>]`: Włącz wymuszanie ssl lub nie wymusz w przypadku łączenia się z serwerem.</span><span class="sxs-lookup"><span data-stu-id="ff388-161">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="ff388-162">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="ff388-162">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="ff388-163">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włącz funkcję nadmiarowej lokalizacji geograficznej lub nie umożliwia tworzenia kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="ff388-163">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="ff388-164">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff388-164">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="ff388-165">`[StorageProfileStorageMb <Int32?>]`: Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="ff388-165">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="ff388-166">`[UserVisibleState <ServerState?>]`: stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ff388-166">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="ff388-167">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="ff388-167">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="ff388-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff388-168">RELATED LINKS</span></span>

