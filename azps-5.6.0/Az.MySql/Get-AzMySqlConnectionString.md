---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: c85ece43045144d0befd6a6ed1e7ac1d7431796f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010449"
---
# <span data-ttu-id="bb8cc-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="bb8cc-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="bb8cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb8cc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8cc-103">Pobierz parametrów połączenia według dostawcy połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="bb8cc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb8cc-104">SYNTAX</span></span>

### <span data-ttu-id="bb8cc-105">Pobierz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bb8cc-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bb8cc-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bb8cc-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb8cc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb8cc-107">DESCRIPTION</span></span>
<span data-ttu-id="bb8cc-108">Pobierz parametrów połączenia według dostawcy połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="bb8cc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb8cc-109">EXAMPLES</span></span>

### <span data-ttu-id="bb8cc-110">Przykład 1. Uzyskiwanie parametrów połączenia serwera MySql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="bb8cc-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="bb8cc-111">To polecenie cmdlet pobiera ciąg połączenia serwera MySql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="bb8cc-112">Przykład 2. Uzyskiwanie parametrów połączenia serwera MySql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="bb8cc-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="bb8cc-113">To polecenie cmdlet pobiera ciąg połączenia serwera MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="bb8cc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb8cc-114">PARAMETERS</span></span>

### <span data-ttu-id="bb8cc-115">—Klient</span><span class="sxs-lookup"><span data-stu-id="bb8cc-115">-Client</span></span>
<span data-ttu-id="bb8cc-116">Dostawca połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-116">Client connection provider.</span></span>

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

### <span data-ttu-id="bb8cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8cc-117">-DefaultProfile</span></span>
<span data-ttu-id="bb8cc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb8cc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb8cc-119">-InputObject</span></span>
<span data-ttu-id="bb8cc-120">Serwer parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-120">The server for the connection string.</span></span>
<span data-ttu-id="bb8cc-121">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb8cc-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bb8cc-122">-Name</span></span>
<span data-ttu-id="bb8cc-123">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-123">The name of the server.</span></span>

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

### <span data-ttu-id="bb8cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb8cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb8cc-125">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="bb8cc-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb8cc-126">-SubscriptionId</span></span>
<span data-ttu-id="bb8cc-127">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="bb8cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8cc-128">CommonParameters</span></span>
<span data-ttu-id="bb8cc-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8cc-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb8cc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8cc-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb8cc-131">INPUTS</span></span>

### <span data-ttu-id="bb8cc-132">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iServer</span><span class="sxs-lookup"><span data-stu-id="bb8cc-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="bb8cc-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb8cc-133">OUTPUTS</span></span>

### <span data-ttu-id="bb8cc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bb8cc-134">System.String</span></span>

## <span data-ttu-id="bb8cc-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb8cc-135">NOTES</span></span>

<span data-ttu-id="bb8cc-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="bb8cc-136">ALIASES</span></span>

<span data-ttu-id="bb8cc-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb8cc-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb8cc-138">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb8cc-139">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb8cc-140">INPUTOBJECT: <IServer> Serwer parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-140">INPUTOBJECT <IServer>: The server for the connection string.</span></span>
  - <span data-ttu-id="bb8cc-141">`Location <String>`: lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="bb8cc-141">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="bb8cc-142">`[Tag <ITrackedResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-142">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="bb8cc-143">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bb8cc-144">`[AdministratorLogin <String>]`: nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="bb8cc-145">Można określić tylko wtedy, gdy serwer jest tworzony (i jest wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="bb8cc-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="bb8cc-146">`[EarliestRestoreDate <DateTime?>]`: najwcześniejszy czas tworzenia punktów przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="bb8cc-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="bb8cc-147">`[FullyQualifiedDomainName <String>]`: w pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="bb8cc-148">`[IdentityType <IdentityType?>]`: typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="bb8cc-149">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać do zasobu podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="bb8cc-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stan pokazujący, czy szyfrowanie infrastruktury było włączone dla serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="bb8cc-151">`[MasterServerId <String>]`: Główny identyfikator serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="bb8cc-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: wymuszanie minimalnej wersji Tls dla serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="bb8cc-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: czy na tym serwerze jest dozwolony dostęp do sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="bb8cc-154">Wartość jest opcjonalna, ale jeśli zostanie przekazana, musi mieć wartość "Włączona" lub "Wyłączona".</span><span class="sxs-lookup"><span data-stu-id="bb8cc-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="bb8cc-155">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="bb8cc-156">`[ReplicationRole <String>]`: rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="bb8cc-157">`[SkuCapacity <Int32?>]`: Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="bb8cc-158">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="bb8cc-159">`[SkuName <String>]`: nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="bb8cc-160">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany przez zasób w zależności od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="bb8cc-161">`[SkuTier <SkuTier?>]`: warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="bb8cc-162">`[SslEnforcement <SslEnforcementEnum?>]`: Włącz wymuszanie ssl lub nie wymusz w przypadku łączenia się z serwerem.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="bb8cc-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="bb8cc-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włącz funkcję nadmiarowej lokalizacji geograficznej lub nie umożliwia tworzenia kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="bb8cc-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="bb8cc-166">`[StorageProfileStorageMb <Int32?>]`: Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="bb8cc-167">`[UserVisibleState <ServerState?>]`: stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="bb8cc-168">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="bb8cc-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="bb8cc-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb8cc-169">RELATED LINKS</span></span>

