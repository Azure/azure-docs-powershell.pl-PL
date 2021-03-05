---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 17e6c492828f877ebf53c634a7670e8d60c9ccba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995030"
---
# <span data-ttu-id="5c31d-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c31d-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="5c31d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c31d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c31d-103">Ustawia właściwości bazy danych lub przenosi istniejącą bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="5c31d-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="5c31d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5c31d-104">SYNTAX</span></span>

### <span data-ttu-id="5c31d-105">Aktualizacja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="5c31d-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c31d-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="5c31d-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c31d-107">Zmień nazwę</span><span class="sxs-lookup"><span data-stu-id="5c31d-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c31d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5c31d-108">DESCRIPTION</span></span>
<span data-ttu-id="5c31d-109">Polecenie **cmdlet Set-AzSqlDatabase** ustawia właściwości bazy danych w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5c31d-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="5c31d-110">To polecenie cmdlet może modyfikować warstwę usługi *(Edition),* poziom wydajności *(RequestedServiceObjectiveName)* i maksymalny rozmiar magazynu *(MaxSizeBytes)* bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5c31d-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="5c31d-111">Ponadto można określić parametr *JSWD,* aby przenieść bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="5c31d-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="5c31d-112">Jeśli baza danych znajduje się już w elastycznej puli, można użyć parametru *RequestedServiceObjectiveName* w celu przeniesienia bazy danych z puli elastycznej i na poziom wydajności dla pojedynczych baz danych.</span><span class="sxs-lookup"><span data-stu-id="5c31d-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="5c31d-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5c31d-113">EXAMPLES</span></span>

### <span data-ttu-id="5c31d-114">Przykład 1. Aktualizowanie bazy danych do bazy danych standardowa S0</span><span class="sxs-lookup"><span data-stu-id="5c31d-114">Example 1: Update a database to a Standard S0 database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S0"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="5c31d-115">To polecenie aktualizuje bazę danych o nazwie Database01 na standardową bazę danych S0 na serwerze o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="5c31d-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="5c31d-116">Przykład 2. Dodawanie bazy danych do elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="5c31d-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="5c31d-117">To polecenie powoduje dodanie bazy danych o nazwie Database01 do puli elastycznej o nazwie Chembojna Bufor01 hostowanej na serwerze o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="5c31d-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="5c31d-118">Przykład 3. Modyfikowanie maksymalnego rozmiaru miejsca do magazynowania bazy danych</span><span class="sxs-lookup"><span data-stu-id="5c31d-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="5c31d-119">To polecenie aktualizuje bazę danych o nazwie Database01, aby ustawić jej maksymalny rozmiar na 1 TB.</span><span class="sxs-lookup"><span data-stu-id="5c31d-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="5c31d-120">Przykład 4. Aktualizowanie istniejącej bazy danych ogólnego przeznaczenia do warstwy usługi w skali hiperskalowej</span><span class="sxs-lookup"><span data-stu-id="5c31d-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Hyperscale" -RequestedServiceObjectiveName "HS_Gen5_2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : 56246136-839f-4171-80af-4c28142463b1
Edition                       : Hyperscale
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : -1
Status                        : Online
CreationDate                  : 12/6/2020 5:34:16 PM
CurrentServiceObjectiveId     : 00000000-0000-0000-0000-000000000000
CurrentServiceObjectiveName   : HS_Gen5_2
RequestedServiceObjectiveName : HS_Gen5_2
RequestedServiceObjectiveId   :
ElasticPoolName               :
EarliestRestoreDate           : 12/6/2020 5:34:16 PM
Tags                          : {}
ResourceId                    : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/Server01/databases/Database01
CreateMode                    :
ReadScale                     : Enabled
ZoneRedundant                 :
Capacity                      : 2
Family                        : Gen5
SkuName                       : HS_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       :
MinimumCapacity               :
ReadReplicaCount              : 1
BackupStorageRedundancy       : Geo
```

<span data-ttu-id="5c31d-121">To polecenie aktualizuje bazę danych o nazwie Database01 z bazy danych ogólnego przeznaczenia do warstwy usługi w skali hiperskalowej.</span><span class="sxs-lookup"><span data-stu-id="5c31d-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="5c31d-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c31d-122">PARAMETERS</span></span>

### <span data-ttu-id="5c31d-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5c31d-123">-AsJob</span></span>
<span data-ttu-id="5c31d-124">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5c31d-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c31d-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="5c31d-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="5c31d-126">Opóźnienie automatycznego wstrzymania w minutach w przypadku bazy danych (tylko bez serwera), -1 w celu rezygnacji</span><span class="sxs-lookup"><span data-stu-id="5c31d-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="5c31d-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="5c31d-128">Nadmiarowość magazynu kopii zapasowej używana do przechowywania kopii zapasowych dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5c31d-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="5c31d-129">Dostępne są następujące opcje: Lokalny, Strefa i Geo.</span><span class="sxs-lookup"><span data-stu-id="5c31d-129">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-130">-Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="5c31d-130">-ComputeGeneration</span></span>
<span data-ttu-id="5c31d-131">Generowanie obliczeniowe do przypisania.</span><span class="sxs-lookup"><span data-stu-id="5c31d-131">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-132">- ComputeModel</span><span class="sxs-lookup"><span data-stu-id="5c31d-132">-ComputeModel</span></span>
<span data-ttu-id="5c31d-133">Obliczany model bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="5c31d-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="5c31d-134">Bez serwera lub z inicjowaniem obsługi administracyjnej</span><span class="sxs-lookup"><span data-stu-id="5c31d-134">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c31d-135">-DatabaseName</span></span>
<span data-ttu-id="5c31d-136">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5c31d-136">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c31d-137">-DefaultProfile</span></span>
<span data-ttu-id="5c31d-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5c31d-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-139">— wersja</span><span class="sxs-lookup"><span data-stu-id="5c31d-139">-Edition</span></span>
<span data-ttu-id="5c31d-140">Określa wersję bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5c31d-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="5c31d-141">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5c31d-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c31d-142">Brak</span><span class="sxs-lookup"><span data-stu-id="5c31d-142">None</span></span>
- <span data-ttu-id="5c31d-143">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="5c31d-143">Basic</span></span>
- <span data-ttu-id="5c31d-144">Standardowe</span><span class="sxs-lookup"><span data-stu-id="5c31d-144">Standard</span></span>
- <span data-ttu-id="5c31d-145">Premium</span><span class="sxs-lookup"><span data-stu-id="5c31d-145">Premium</span></span>
- <span data-ttu-id="5c31d-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="5c31d-146">DataWarehouse</span></span>
- <span data-ttu-id="5c31d-147">Bezpłatne</span><span class="sxs-lookup"><span data-stu-id="5c31d-147">Free</span></span>
- <span data-ttu-id="5c31d-148">Rozciągnięcie</span><span class="sxs-lookup"><span data-stu-id="5c31d-148">Stretch</span></span>
- <span data-ttu-id="5c31d-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="5c31d-149">GeneralPurpose</span></span>
- <span data-ttu-id="5c31d-150">Skala hiperskali</span><span class="sxs-lookup"><span data-stu-id="5c31d-150">Hyperscale</span></span>
- <span data-ttu-id="5c31d-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="5c31d-151">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-152">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="5c31d-152">-ElasticPoolName</span></span>
<span data-ttu-id="5c31d-153">Określa nazwę puli elastycznej, do której ma być przesunana baza danych.</span><span class="sxs-lookup"><span data-stu-id="5c31d-153">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5c31d-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="5c31d-155">Liczba tylko replik pomocniczych skojarzonych z bazą danych.</span><span class="sxs-lookup"><span data-stu-id="5c31d-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="5c31d-156">Dotyczy tylko wersji Hyperscale.</span><span class="sxs-lookup"><span data-stu-id="5c31d-156">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5c31d-157">-LicenseType</span></span>
<span data-ttu-id="5c31d-158">Typ licencji dla bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="5c31d-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="5c31d-159">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="5c31d-159">Possible values are:</span></span>
- <span data-ttu-id="5c31d-160">Cena Bazowa — zastosowano rabat w ramach korzyści hybrydowej platformy Azure (AHB) dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c31d-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="5c31d-161">Cena bazy danych zostanie z rabatem dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c31d-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="5c31d-162">Cena rabatu z rabatem na usługę Azure Hybrid Benefit (AHB) dla istniejących właścicieli licencji programu SQL Server nie jest stosowana.</span><span class="sxs-lookup"><span data-stu-id="5c31d-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="5c31d-163">Cena bazy danych będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c31d-163">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-164">- MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5c31d-164">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="5c31d-165">Identyfikator konfiguracji konserwacji bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5c31d-165">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="5c31d-166">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="5c31d-166">-MaxSizeBytes</span></span>
<span data-ttu-id="5c31d-167">Maksymalny rozmiar bazy danych Azure SQL Database w bajtach.</span><span class="sxs-lookup"><span data-stu-id="5c31d-167">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-168">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="5c31d-168">-MinimumCapacity</span></span>
<span data-ttu-id="5c31d-169">Minimalna pojemność, która będzie przydzielana przez bazę danych, jeśli nie zostanie wstrzymana.</span><span class="sxs-lookup"><span data-stu-id="5c31d-169">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="5c31d-170">Tylko bazy danych Azure Sql bez serwera.</span><span class="sxs-lookup"><span data-stu-id="5c31d-170">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-171">-NewName</span><span class="sxs-lookup"><span data-stu-id="5c31d-171">-NewName</span></span>
<span data-ttu-id="5c31d-172">Nowa nazwa, na która ma zostać zmieniona nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5c31d-172">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="5c31d-173">-ReadScale</span></span>
<span data-ttu-id="5c31d-174">Jeśli ta funkcja jest włączona, połączenia, dla których celem aplikacji ustawiono odczyt tylko do odczytu w ciągu połączenia, mogą być kierowane do repliki pomocniczej tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="5c31d-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="5c31d-175">Tę właściwość można ustawiać tylko w przypadku baz danych o krytycznym znaczeniu dla wersji Premium i Business.</span><span class="sxs-lookup"><span data-stu-id="5c31d-175">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="5c31d-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="5c31d-177">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5c31d-177">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="5c31d-178">Aby uzyskać informacje na temat celów usługi, zobacz warstwy usług [azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) i poziomy wydajności w bibliotece sieci deweloperskiej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5c31d-178">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c31d-179">-ResourceGroupName</span></span>
<span data-ttu-id="5c31d-180">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="5c31d-180">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-181">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="5c31d-181">-SecondaryType</span></span>
<span data-ttu-id="5c31d-182">Pomocniczy typ bazy danych, jeśli jest to pomocniczy typ bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5c31d-182">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="5c31d-183">Prawidłowe wartości to Geo i Named.</span><span class="sxs-lookup"><span data-stu-id="5c31d-183">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-184">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c31d-184">-ServerName</span></span>
<span data-ttu-id="5c31d-185">Określa nazwę serwera hostowego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="5c31d-185">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-186">— Tagi</span><span class="sxs-lookup"><span data-stu-id="5c31d-186">-Tags</span></span>
<span data-ttu-id="5c31d-187">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="5c31d-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5c31d-188">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5c31d-188">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-189">— VCore</span><span class="sxs-lookup"><span data-stu-id="5c31d-189">-VCore</span></span>
<span data-ttu-id="5c31d-190">Numer Vcore bazy danych Azure Sql Database</span><span class="sxs-lookup"><span data-stu-id="5c31d-190">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-191">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="5c31d-191">-ZoneRedundant</span></span>
<span data-ttu-id="5c31d-192">Nadmiarowość stref do skojarzenia z usługą Azure Sql Database</span><span class="sxs-lookup"><span data-stu-id="5c31d-192">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-193">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c31d-193">-Confirm</span></span>
<span data-ttu-id="5c31d-194">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5c31d-194">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c31d-195">-WhatIf</span></span>
<span data-ttu-id="5c31d-196">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c31d-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c31d-197">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5c31d-197">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c31d-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c31d-198">CommonParameters</span></span>
<span data-ttu-id="5c31d-199">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c31d-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c31d-200">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c31d-200">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c31d-201">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c31d-201">INPUTS</span></span>

### <span data-ttu-id="5c31d-202">System.String</span><span class="sxs-lookup"><span data-stu-id="5c31d-202">System.String</span></span>

## <span data-ttu-id="5c31d-203">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c31d-203">OUTPUTS</span></span>

### <span data-ttu-id="5c31d-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5c31d-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5c31d-205">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5c31d-205">NOTES</span></span>

## <span data-ttu-id="5c31d-206">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c31d-206">RELATED LINKS</span></span>

[<span data-ttu-id="5c31d-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c31d-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="5c31d-208">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c31d-208">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="5c31d-209">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c31d-209">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="5c31d-210">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c31d-210">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5c31d-211">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c31d-211">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="5c31d-212">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5c31d-212">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
