---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 2fefc797cc17ca6971c05027a2e3badac8a10045
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995436"
---
# <span data-ttu-id="99173-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="99173-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="99173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99173-102">SYNOPSIS</span></span>
<span data-ttu-id="99173-103">Tworzy nową replikę z istniejącej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="99173-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="99173-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99173-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="99173-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="99173-105">DESCRIPTION</span></span>
<span data-ttu-id="99173-106">Tworzy nową replikę z istniejącej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="99173-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="99173-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99173-107">EXAMPLES</span></span>

### <span data-ttu-id="99173-108">Przykład 1. Tworzenie nowej repliki serwera MySql</span><span class="sxs-lookup"><span data-stu-id="99173-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="99173-109">To polecenie cmdlet tworzy nową replikę serwera MySql.</span><span class="sxs-lookup"><span data-stu-id="99173-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="99173-110">Przykład 2. Tworzenie nowej repliki serwera MySql</span><span class="sxs-lookup"><span data-stu-id="99173-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="99173-111">To polecenie cmdlet z wzorcem parametrów(inputobject) tworzy nową replikę serwera MySql.</span><span class="sxs-lookup"><span data-stu-id="99173-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="99173-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99173-112">PARAMETERS</span></span>

### <span data-ttu-id="99173-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="99173-113">-AsJob</span></span>
<span data-ttu-id="99173-114">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="99173-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="99173-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99173-115">-DefaultProfile</span></span>
<span data-ttu-id="99173-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99173-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99173-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="99173-117">-Location</span></span>
<span data-ttu-id="99173-118">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="99173-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="99173-119">— Wzorzec</span><span class="sxs-lookup"><span data-stu-id="99173-119">-Master</span></span>
<span data-ttu-id="99173-120">Obiekt serwera źródłowego, z którym ma być tworzyć repliki.</span><span class="sxs-lookup"><span data-stu-id="99173-120">The source server object to create replica from.</span></span>
<span data-ttu-id="99173-121">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach wzorca i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="99173-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="99173-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="99173-122">-NoWait</span></span>
<span data-ttu-id="99173-123">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="99173-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="99173-124">— Replika</span><span class="sxs-lookup"><span data-stu-id="99173-124">-Replica</span></span>
<span data-ttu-id="99173-125">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="99173-125">The name of the server.</span></span>

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

### <span data-ttu-id="99173-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99173-126">-ResourceGroupName</span></span>
<span data-ttu-id="99173-127">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="99173-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="99173-128">- SKU</span><span class="sxs-lookup"><span data-stu-id="99173-128">-Sku</span></span>
<span data-ttu-id="99173-129">Nazwa sKU, zwykle warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="99173-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="99173-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99173-130">-SubscriptionId</span></span>
<span data-ttu-id="99173-131">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="99173-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="99173-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99173-132">-Confirm</span></span>
<span data-ttu-id="99173-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99173-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99173-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99173-134">-WhatIf</span></span>
<span data-ttu-id="99173-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99173-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99173-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="99173-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99173-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99173-137">CommonParameters</span></span>
<span data-ttu-id="99173-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99173-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99173-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99173-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99173-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99173-140">INPUTS</span></span>

### <span data-ttu-id="99173-141">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iServer</span><span class="sxs-lookup"><span data-stu-id="99173-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="99173-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99173-142">OUTPUTS</span></span>

### <span data-ttu-id="99173-143">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iServer</span><span class="sxs-lookup"><span data-stu-id="99173-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="99173-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99173-144">NOTES</span></span>

<span data-ttu-id="99173-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="99173-145">ALIASES</span></span>

<span data-ttu-id="99173-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99173-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99173-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="99173-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99173-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99173-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99173-149">MASTER: <IServer> obiekt serwera źródłowego, z którym ma być tworzyć repliki.</span><span class="sxs-lookup"><span data-stu-id="99173-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="99173-150">`Location <String>`: lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="99173-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="99173-151">`[Tag <ITrackedResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="99173-151">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="99173-152">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="99173-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="99173-153">`[AdministratorLogin <String>]`: nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="99173-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="99173-154">Można określić tylko wtedy, gdy serwer jest tworzony (i jest wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="99173-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="99173-155">`[EarliestRestoreDate <DateTime?>]`: najwcześniejszy czas tworzenia punktów przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="99173-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="99173-156">`[FullyQualifiedDomainName <String>]`: w pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="99173-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="99173-157">`[IdentityType <IdentityType?>]`: typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="99173-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="99173-158">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać do zasobu podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="99173-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="99173-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stan pokazujący, czy szyfrowanie infrastruktury było włączone dla serwera.</span><span class="sxs-lookup"><span data-stu-id="99173-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="99173-160">`[MasterServerId <String>]`: Główny identyfikator serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="99173-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="99173-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: wymuszanie minimalnej wersji Tls dla serwera.</span><span class="sxs-lookup"><span data-stu-id="99173-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="99173-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: czy na tym serwerze jest dozwolony dostęp do sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="99173-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="99173-163">Wartość jest opcjonalna, ale jeśli zostanie przekazana, musi mieć wartość "Włączona" lub "Wyłączona".</span><span class="sxs-lookup"><span data-stu-id="99173-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="99173-164">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="99173-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="99173-165">`[ReplicationRole <String>]`: rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="99173-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="99173-166">`[SkuCapacity <Int32?>]`: Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.</span><span class="sxs-lookup"><span data-stu-id="99173-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="99173-167">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="99173-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="99173-168">`[SkuName <String>]`: nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="99173-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="99173-169">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany przez zasób w zależności od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="99173-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="99173-170">`[SkuTier <SkuTier?>]`: warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="99173-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="99173-171">`[SslEnforcement <SslEnforcementEnum?>]`: Włącz wymuszanie ssl lub nie wymusz w przypadku łączenia się z serwerem.</span><span class="sxs-lookup"><span data-stu-id="99173-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="99173-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="99173-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="99173-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włącz funkcję nadmiarowej lokalizacji geograficznej lub nie umożliwia tworzenia kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="99173-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="99173-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="99173-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="99173-175">`[StorageProfileStorageMb <Int32?>]`: Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="99173-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="99173-176">`[UserVisibleState <ServerState?>]`: stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="99173-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="99173-177">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="99173-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="99173-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99173-178">RELATED LINKS</span></span>

