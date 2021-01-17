---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 6d737abb6c58ea8c74085f8390d7a6acbdf54dc8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376453"
---
# <span data-ttu-id="70f25-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70f25-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="70f25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70f25-102">SYNOPSIS</span></span>
<span data-ttu-id="70f25-103">Ustawia właściwości bazy danych lub przenosi istniejącą bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="70f25-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="70f25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70f25-104">SYNTAX</span></span>

### <span data-ttu-id="70f25-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="70f25-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70f25-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="70f25-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70f25-107">Nazwy</span><span class="sxs-lookup"><span data-stu-id="70f25-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70f25-108">Opis</span><span class="sxs-lookup"><span data-stu-id="70f25-108">DESCRIPTION</span></span>
<span data-ttu-id="70f25-109">Polecenie cmdlet **Set-AzSqlDatabase** ustawia właściwości bazy danych w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="70f25-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="70f25-110">To polecenie cmdlet może zmodyfikować warstwę usług (*wersja*), poziom wydajności (*RequestedServiceObjectiveName*) i maksymalny rozmiar magazynu (*MaxSizeBytes*) bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70f25-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="70f25-111">Ponadto można określić parametr *ElasticPoolName* , aby przenieść bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="70f25-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="70f25-112">Jeśli baza danych znajduje się już w puli elastycznej, można użyć parametru *RequestedServiceObjectiveName* , aby przenieść bazę danych poza elastyczną pulę i na poziom wydajności dla pojedynczych baz danych.</span><span class="sxs-lookup"><span data-stu-id="70f25-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="70f25-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70f25-113">EXAMPLES</span></span>

### <span data-ttu-id="70f25-114">Przykład 1: aktualizowanie bazy danych do standardowej bazy danych S0</span><span class="sxs-lookup"><span data-stu-id="70f25-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="70f25-115">To polecenie aktualizuje bazę danych o nazwie Database01 do standardowej bazy danych S0 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="70f25-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="70f25-116">Przykład 2: Dodawanie bazy danych do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="70f25-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="70f25-117">To polecenie dodaje bazę danych o nazwie Database01 do puli elastycznej o nazwie ElasticPool01 hostowanej na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="70f25-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="70f25-118">Przykład 3: modyfikowanie maksymalnego rozmiaru przestrzeni dyskowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="70f25-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="70f25-119">To polecenie aktualizuje bazę danych o nazwie Database01, aby ustawić jej maksymalny rozmiar na 1 TB.</span><span class="sxs-lookup"><span data-stu-id="70f25-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="70f25-120">Przykład 4: aktualizowanie istniejącej bazy danych ogólnego przeznaczenia w celu przeskalowania warstwy usługi</span><span class="sxs-lookup"><span data-stu-id="70f25-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
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

<span data-ttu-id="70f25-121">To polecenie aktualizuje bazę danych o nazwie Database01 w ogólnym celu w celu przedskalowania warstwy usługi.</span><span class="sxs-lookup"><span data-stu-id="70f25-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="70f25-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70f25-122">PARAMETERS</span></span>

### <span data-ttu-id="70f25-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70f25-123">-AsJob</span></span>
<span data-ttu-id="70f25-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="70f25-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70f25-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="70f25-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="70f25-126">Opóźnienie automatycznego wstrzymania w minutach dla bazy danych (tylko na serwerze),-1 w celu rezygnacji</span><span class="sxs-lookup"><span data-stu-id="70f25-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="70f25-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="70f25-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="70f25-128">Nadmiarowość miejsca do magazynowania kopii zapasowej używana do przechowywania kopii zapasowych bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="70f25-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="70f25-129">Dostępne opcje: local, Zone i geo.</span><span class="sxs-lookup"><span data-stu-id="70f25-129">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="70f25-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="70f25-130">-ComputeGeneration</span></span>
<span data-ttu-id="70f25-131">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="70f25-131">The compute generation to assign.</span></span>

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

### <span data-ttu-id="70f25-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="70f25-132">-ComputeModel</span></span>
<span data-ttu-id="70f25-133">Obliczony model bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="70f25-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="70f25-134">Serwer lub Zainicjowano obsługę administracyjną</span><span class="sxs-lookup"><span data-stu-id="70f25-134">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="70f25-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70f25-135">-DatabaseName</span></span>
<span data-ttu-id="70f25-136">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70f25-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="70f25-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f25-137">-DefaultProfile</span></span>
<span data-ttu-id="70f25-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="70f25-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70f25-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="70f25-139">-Edition</span></span>
<span data-ttu-id="70f25-140">Określa wersję bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70f25-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="70f25-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="70f25-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70f25-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="70f25-142">None</span></span>
- <span data-ttu-id="70f25-143">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="70f25-143">Basic</span></span>
- <span data-ttu-id="70f25-144">Standard</span><span class="sxs-lookup"><span data-stu-id="70f25-144">Standard</span></span>
- <span data-ttu-id="70f25-145">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="70f25-145">Premium</span></span>
- <span data-ttu-id="70f25-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="70f25-146">DataWarehouse</span></span>
- <span data-ttu-id="70f25-147">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="70f25-147">Free</span></span>
- <span data-ttu-id="70f25-148">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="70f25-148">Stretch</span></span>
- <span data-ttu-id="70f25-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="70f25-149">GeneralPurpose</span></span>
- <span data-ttu-id="70f25-150">Podskalowanie</span><span class="sxs-lookup"><span data-stu-id="70f25-150">Hyperscale</span></span>
- <span data-ttu-id="70f25-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="70f25-151">BusinessCritical</span></span>

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

### <span data-ttu-id="70f25-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="70f25-152">-ElasticPoolName</span></span>
<span data-ttu-id="70f25-153">Określa nazwę puli elastycznej, w której ma zostać przeniesiona baza danych.</span><span class="sxs-lookup"><span data-stu-id="70f25-153">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="70f25-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="70f25-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="70f25-155">Liczba replik pomocniczych tylko do odczytu skojarzonych z bazą danych.</span><span class="sxs-lookup"><span data-stu-id="70f25-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="70f25-156">Dotyczy tylko wersji z podskalą.</span><span class="sxs-lookup"><span data-stu-id="70f25-156">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="70f25-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="70f25-157">-LicenseType</span></span>
<span data-ttu-id="70f25-158">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="70f25-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="70f25-159">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="70f25-159">Possible values are:</span></span>
- <span data-ttu-id="70f25-160">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="70f25-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="70f25-161">Cena bazy danych zostanie obniżona o istniejące właściciele licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="70f25-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="70f25-162">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="70f25-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="70f25-163">Cena bazy danych będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="70f25-163">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="70f25-164">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="70f25-164">-MaxSizeBytes</span></span>
<span data-ttu-id="70f25-165">Maksymalny rozmiar bazy danych SQL Azure w bajtach.</span><span class="sxs-lookup"><span data-stu-id="70f25-165">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="70f25-166">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="70f25-166">-MinimumCapacity</span></span>
<span data-ttu-id="70f25-167">Minimalna pojemność bazy danych jest zawsze przydzielona, jeśli nie została wstrzymana.</span><span class="sxs-lookup"><span data-stu-id="70f25-167">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="70f25-168">W przypadku baz danych platformy Azure SQL bezserwerowych.</span><span class="sxs-lookup"><span data-stu-id="70f25-168">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="70f25-169">-NewName</span><span class="sxs-lookup"><span data-stu-id="70f25-169">-NewName</span></span>
<span data-ttu-id="70f25-170">Nowa nazwa, do której ma zostać zmieniona baza danych.</span><span class="sxs-lookup"><span data-stu-id="70f25-170">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="70f25-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="70f25-171">-ReadScale</span></span>
<span data-ttu-id="70f25-172">Jeśli ta opcja jest włączona, połączenia z zastosowanymi aplikacjami, które mają ustawioną wartość tylko do odczytu, mogą być przekierowywane do repliki pomocniczej tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="70f25-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="70f25-173">Ta właściwość jest tylko do settable dla kluczowych baz danych Premium i dla firm.</span><span class="sxs-lookup"><span data-stu-id="70f25-173">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="70f25-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="70f25-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="70f25-175">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70f25-175">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="70f25-176">Aby uzyskać informacje na temat celów usługi, zobacz [warstwy usług Azure SQL Database i poziomy wydajności](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="70f25-176">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="70f25-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f25-177">-ResourceGroupName</span></span>
<span data-ttu-id="70f25-178">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="70f25-178">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="70f25-179">-Drugorzędny</span><span class="sxs-lookup"><span data-stu-id="70f25-179">-SecondaryType</span></span>
<span data-ttu-id="70f25-180">Pomocniczy typ bazy danych, jeśli jest pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="70f25-180">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="70f25-181">Prawidłowe wartości to Geo i Named.</span><span class="sxs-lookup"><span data-stu-id="70f25-181">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="70f25-182">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="70f25-182">-ServerName</span></span>
<span data-ttu-id="70f25-183">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="70f25-183">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="70f25-184">-Tagi</span><span class="sxs-lookup"><span data-stu-id="70f25-184">-Tags</span></span>
<span data-ttu-id="70f25-185">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="70f25-185">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="70f25-186">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="70f25-186">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="70f25-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="70f25-187">-VCore</span></span>
<span data-ttu-id="70f25-188">Numer vCore bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="70f25-188">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="70f25-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="70f25-189">-ZoneRedundant</span></span>
<span data-ttu-id="70f25-190">Nadmiarowość strefy do skojarzenia z bazą danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="70f25-190">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="70f25-191">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70f25-191">-Confirm</span></span>
<span data-ttu-id="70f25-192">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70f25-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f25-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f25-193">-WhatIf</span></span>
<span data-ttu-id="70f25-194">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70f25-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70f25-195">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70f25-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70f25-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f25-196">CommonParameters</span></span>
<span data-ttu-id="70f25-197">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f25-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f25-198">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70f25-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f25-199">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70f25-199">INPUTS</span></span>

### <span data-ttu-id="70f25-200">System. String</span><span class="sxs-lookup"><span data-stu-id="70f25-200">System.String</span></span>

## <span data-ttu-id="70f25-201">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70f25-201">OUTPUTS</span></span>

### <span data-ttu-id="70f25-202">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="70f25-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="70f25-203">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70f25-203">NOTES</span></span>

## <span data-ttu-id="70f25-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70f25-204">RELATED LINKS</span></span>

[<span data-ttu-id="70f25-205">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70f25-205">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="70f25-206">Nowe — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70f25-206">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="70f25-207">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70f25-207">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="70f25-208">Życiorys — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70f25-208">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="70f25-209">Suspend — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70f25-209">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="70f25-210">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="70f25-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
