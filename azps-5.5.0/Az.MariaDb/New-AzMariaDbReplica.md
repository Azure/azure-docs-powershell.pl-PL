---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185130"
---
# <span data-ttu-id="cb2d4-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="cb2d4-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="cb2d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb2d4-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2d4-103">Tworzy replikę serwera MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="cb2d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cb2d4-104">SYNTAX</span></span>

### <span data-ttu-id="cb2d4-105">Nazwa_serwera (domyślna)</span><span class="sxs-lookup"><span data-stu-id="cb2d4-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb2d4-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="cb2d4-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cb2d4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cb2d4-107">DESCRIPTION</span></span>
<span data-ttu-id="cb2d4-108">Tworzy replikę serwera MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="cb2d4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cb2d4-109">EXAMPLES</span></span>

### <span data-ttu-id="cb2d4-110">Przykład 1. Tworzenie repliki bazy danych dla bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="cb2d4-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="cb2d4-111">To polecenie tworzy replikę bazy danych dla bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="cb2d4-112">Przykład 2. Tworzenie repliki bazy danych dla bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="cb2d4-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="cb2d4-113">To polecenie tworzy replikę bazy danych dla bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="cb2d4-114">Przykład 3. Tworzenie repliki bazy danych dla bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="cb2d4-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="cb2d4-115">To polecenie z parametrem inputobject tworzy replikę bazy danych z parametrem inputobject dla bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="cb2d4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb2d4-116">PARAMETERS</span></span>

### <span data-ttu-id="cb2d4-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cb2d4-117">-AsJob</span></span>
<span data-ttu-id="cb2d4-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="cb2d4-118">Run the command as a job</span></span>

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

### <span data-ttu-id="cb2d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2d4-119">-DefaultProfile</span></span>
<span data-ttu-id="cb2d4-120">Region DefaultParameters Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb2d4-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cb2d4-121">-Location</span></span>
<span data-ttu-id="cb2d4-122">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="cb2d4-123">— Wzorzec</span><span class="sxs-lookup"><span data-stu-id="cb2d4-123">-Master</span></span>
<span data-ttu-id="cb2d4-124">Obiekt serwera źródłowego, z którym chcesz przywrócić dane.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-124">The source server object to restore from.</span></span>
<span data-ttu-id="cb2d4-125">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach wzorca i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb2d4-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="cb2d4-126">-MasterName</span></span>
<span data-ttu-id="cb2d4-127">Nazwa serwera MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="cb2d4-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cb2d4-128">-NoWait</span></span>
<span data-ttu-id="cb2d4-129">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="cb2d4-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cb2d4-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="cb2d4-130">-ReplicaName</span></span>
<span data-ttu-id="cb2d4-131">Nazwa repliki.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-131">Replica name.</span></span>

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

### <span data-ttu-id="cb2d4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb2d4-132">-ResourceGroupName</span></span>
<span data-ttu-id="cb2d4-133">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cb2d4-134">- SKU</span><span class="sxs-lookup"><span data-stu-id="cb2d4-134">-Sku</span></span>
<span data-ttu-id="cb2d4-135">Nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="cb2d4-136">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb2d4-136">-SubscriptionId</span></span>
<span data-ttu-id="cb2d4-137">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cb2d4-138">— Tag</span><span class="sxs-lookup"><span data-stu-id="cb2d4-138">-Tag</span></span>
<span data-ttu-id="cb2d4-139">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="cb2d4-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb2d4-140">-Confirm</span></span>
<span data-ttu-id="cb2d4-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb2d4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb2d4-142">-WhatIf</span></span>
<span data-ttu-id="cb2d4-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb2d4-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb2d4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2d4-145">CommonParameters</span></span>
<span data-ttu-id="cb2d4-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2d4-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb2d4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2d4-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb2d4-148">INPUTS</span></span>

### <span data-ttu-id="cb2d4-149">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="cb2d4-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="cb2d4-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb2d4-150">OUTPUTS</span></span>

### <span data-ttu-id="cb2d4-151">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="cb2d4-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="cb2d4-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cb2d4-152">NOTES</span></span>

<span data-ttu-id="cb2d4-153">ALIASY</span><span class="sxs-lookup"><span data-stu-id="cb2d4-153">ALIASES</span></span>

<span data-ttu-id="cb2d4-154">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb2d4-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb2d4-155">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb2d4-156">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb2d4-157">MASTER: <IServer> obiekt serwera źródłowego, z którym chcesz przywrócić dane.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="cb2d4-158">`Location <String>`: lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="cb2d4-159">`[Tag <ITrackedResourceTags>]`: metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="cb2d4-160">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cb2d4-161">`[AdministratorLogin <String>]`: nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="cb2d4-162">Można określić tylko wtedy, gdy serwer jest tworzony (i jest wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="cb2d4-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="cb2d4-163">`[EarliestRestoreDate <DateTime?>]`: najwcześniejszy czas tworzenia punktów przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="cb2d4-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="cb2d4-164">`[FullyQualifiedDomainName <String>]`: w pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="cb2d4-165">`[IdentityType <IdentityType?>]`: typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="cb2d4-166">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać do zasobu podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="cb2d4-167">`[MasterServerId <String>]`: Główny identyfikator serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="cb2d4-168">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="cb2d4-169">`[ReplicationRole <String>]`: Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="cb2d4-170">`[SkuCapacity <Int32?>]`: Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="cb2d4-171">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="cb2d4-172">`[SkuName <String>]`: nazwa sKU, zazwyczaj warstwa + rodzina + podstawy, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="cb2d4-173">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany przez zasób w zależności od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="cb2d4-174">`[SkuTier <SkuTier?>]`: warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="cb2d4-175">`[SslEnforcement <SslEnforcementEnum?>]`: Włącz wymuszanie ssl lub nie wymusz w przypadku łączenia się z serwerem.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="cb2d4-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="cb2d4-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włącz funkcję nadmiarowej lokalizacji geograficznej lub nie umożliwia tworzenia kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="cb2d4-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="cb2d4-179">`[StorageProfileStorageMb <Int32?>]`: Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="cb2d4-180">`[UserVisibleState <ServerState?>]`: stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="cb2d4-181">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="cb2d4-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="cb2d4-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb2d4-182">RELATED LINKS</span></span>

