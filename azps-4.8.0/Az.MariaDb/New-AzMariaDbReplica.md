---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222485"
---
# <span data-ttu-id="808b1-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="808b1-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="808b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="808b1-102">SYNOPSIS</span></span>
<span data-ttu-id="808b1-103">Tworzenie repliki serwera MariaDB.</span><span class="sxs-lookup"><span data-stu-id="808b1-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="808b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="808b1-104">SYNTAX</span></span>

### <span data-ttu-id="808b1-105">Nazwa_serwera (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="808b1-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="808b1-106">Serverobject</span><span class="sxs-lookup"><span data-stu-id="808b1-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="808b1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="808b1-107">DESCRIPTION</span></span>
<span data-ttu-id="808b1-108">Tworzenie repliki serwera MariaDB.</span><span class="sxs-lookup"><span data-stu-id="808b1-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="808b1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="808b1-109">EXAMPLES</span></span>

### <span data-ttu-id="808b1-110">Przykład 1. Tworzenie bazy danych repliki dla MariaDB</span><span class="sxs-lookup"><span data-stu-id="808b1-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="808b1-111">To polecenie tworzy bazę danych repliki dla MariaDB.</span><span class="sxs-lookup"><span data-stu-id="808b1-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="808b1-112">Przykład 2: Tworzenie bazy danych repliki dla MariaDB</span><span class="sxs-lookup"><span data-stu-id="808b1-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="808b1-113">To polecenie tworzy bazę danych repliki dla MariaDB.</span><span class="sxs-lookup"><span data-stu-id="808b1-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="808b1-114">Przykład 3: Tworzenie bazy danych repliki dla MariaDB</span><span class="sxs-lookup"><span data-stu-id="808b1-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="808b1-115">To polecenie z parametrem inputobject powoduje utworzenie bazy danych repliki z parametrem inputobject dla MariaDB.</span><span class="sxs-lookup"><span data-stu-id="808b1-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="808b1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="808b1-116">PARAMETERS</span></span>

### <span data-ttu-id="808b1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="808b1-117">-AsJob</span></span>
<span data-ttu-id="808b1-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="808b1-118">Run the command as a job</span></span>

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

### <span data-ttu-id="808b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808b1-119">-DefaultProfile</span></span>
<span data-ttu-id="808b1-120">Region DefaultParameters poświadczenia, konto, dzierżawca i abonament używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="808b1-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="808b1-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="808b1-121">-Location</span></span>
<span data-ttu-id="808b1-122">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="808b1-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="808b1-123">-Master</span><span class="sxs-lookup"><span data-stu-id="808b1-123">-Master</span></span>
<span data-ttu-id="808b1-124">Źródłowy obiekt serwera do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="808b1-124">The source server object to restore from.</span></span>
<span data-ttu-id="808b1-125">Aby skonstruować, zobacz sekcję notatki dla właściwości wzorca i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="808b1-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="808b1-126">-MASTERNAME</span><span class="sxs-lookup"><span data-stu-id="808b1-126">-MasterName</span></span>
<span data-ttu-id="808b1-127">Nazwa serwera MariaDB.</span><span class="sxs-lookup"><span data-stu-id="808b1-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="808b1-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="808b1-128">-NoWait</span></span>
<span data-ttu-id="808b1-129">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="808b1-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="808b1-130">-Replicaname</span><span class="sxs-lookup"><span data-stu-id="808b1-130">-ReplicaName</span></span>
<span data-ttu-id="808b1-131">Nazwa repliki.</span><span class="sxs-lookup"><span data-stu-id="808b1-131">Replica name.</span></span>

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

### <span data-ttu-id="808b1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808b1-132">-ResourceGroupName</span></span>
<span data-ttu-id="808b1-133">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="808b1-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="808b1-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="808b1-134">-Sku</span></span>
<span data-ttu-id="808b1-135">Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="808b1-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="808b1-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="808b1-136">-SubscriptionId</span></span>
<span data-ttu-id="808b1-137">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="808b1-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="808b1-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="808b1-138">-Tag</span></span>
<span data-ttu-id="808b1-139">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="808b1-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="808b1-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="808b1-140">-Confirm</span></span>
<span data-ttu-id="808b1-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="808b1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="808b1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="808b1-142">-WhatIf</span></span>
<span data-ttu-id="808b1-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="808b1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="808b1-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="808b1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="808b1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808b1-145">CommonParameters</span></span>
<span data-ttu-id="808b1-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="808b1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808b1-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="808b1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808b1-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="808b1-148">INPUTS</span></span>

### <span data-ttu-id="808b1-149">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="808b1-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="808b1-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="808b1-150">OUTPUTS</span></span>

### <span data-ttu-id="808b1-151">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="808b1-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="808b1-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="808b1-152">NOTES</span></span>

<span data-ttu-id="808b1-153">PISUJE</span><span class="sxs-lookup"><span data-stu-id="808b1-153">ALIASES</span></span>

<span data-ttu-id="808b1-154">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="808b1-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="808b1-155">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="808b1-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="808b1-156">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="808b1-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="808b1-157">WZORZEC <IServer> : źródłowy obiekt serwera do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="808b1-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="808b1-158">`Location <String>`: Lokalizacja, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="808b1-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="808b1-159">`[Tag <ITrackedResourceTags>]`: Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="808b1-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="808b1-160">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="808b1-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="808b1-161">`[AdministratorLogin <String>]`: Nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="808b1-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="808b1-162">Można określić tylko podczas tworzenia serwera (i jest on wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="808b1-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="808b1-163">`[EarliestRestoreDate <DateTime?>]`: Najwcześniejszy czas tworzenia punktu przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="808b1-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="808b1-164">`[FullyQualifiedDomainName <String>]`: W pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="808b1-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="808b1-165">`[IdentityType <IdentityType?>]`: Typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="808b1-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="808b1-166">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać podmiot zabezpieczeń usługi Azure Active Directory dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="808b1-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="808b1-167">`[MasterServerId <String>]`: Identyfikator głównego serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="808b1-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="808b1-168">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="808b1-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="808b1-169">`[ReplicationRole <String>]`: Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="808b1-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="808b1-170">`[SkuCapacity <Int32?>]`: Wydajność skalowania w górę/poza, reprezentująca jednostki obliczeniowe serwera.</span><span class="sxs-lookup"><span data-stu-id="808b1-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="808b1-171">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="808b1-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="808b1-172">`[SkuName <String>]`: Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="808b1-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="808b1-173">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany według odpowiednich zasobów.</span><span class="sxs-lookup"><span data-stu-id="808b1-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="808b1-174">`[SkuTier <SkuTier?>]`: Warstwa konkretnej jednostki SKU, na przykład podstawowa.</span><span class="sxs-lookup"><span data-stu-id="808b1-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="808b1-175">`[SslEnforcement <SslEnforcementEnum?>]`: Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="808b1-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="808b1-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej serwera.</span><span class="sxs-lookup"><span data-stu-id="808b1-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="808b1-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włączanie geograficznie nadmiarowych lub niezwiązanych z kopią zapasową serwera.</span><span class="sxs-lookup"><span data-stu-id="808b1-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="808b1-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włączanie automatycznego zwiększania przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="808b1-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="808b1-179">`[StorageProfileStorageMb <Int32?>]`: Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="808b1-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="808b1-180">`[UserVisibleState <ServerState?>]`: Stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="808b1-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="808b1-181">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="808b1-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="808b1-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="808b1-182">RELATED LINKS</span></span>

