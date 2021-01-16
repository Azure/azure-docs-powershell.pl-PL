---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 15f9aee8e278a1b33330508a10487e3847820891
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341554"
---
# <span data-ttu-id="3cb8a-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3cb8a-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="3cb8a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cb8a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb8a-103">Ustawia właściwości bazy danych lub przenosi istniejącą bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="3cb8a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cb8a-104">SYNTAX</span></span>

### <span data-ttu-id="3cb8a-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3cb8a-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cb8a-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="3cb8a-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cb8a-107">Nazwy</span><span class="sxs-lookup"><span data-stu-id="3cb8a-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cb8a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3cb8a-108">DESCRIPTION</span></span>
<span data-ttu-id="3cb8a-109">Polecenie cmdlet **Set-AzSqlDatabase** ustawia właściwości bazy danych w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="3cb8a-110">To polecenie cmdlet może zmodyfikować warstwę usług (*wersja*), poziom wydajności (*RequestedServiceObjectiveName*) i maksymalny rozmiar magazynu (*MaxSizeBytes*) bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="3cb8a-111">Ponadto można określić parametr *ElasticPoolName* , aby przenieść bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="3cb8a-112">Jeśli baza danych znajduje się już w puli elastycznej, można użyć parametru *RequestedServiceObjectiveName* , aby przenieść bazę danych poza elastyczną pulę i na poziom wydajności dla pojedynczych baz danych.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="3cb8a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cb8a-113">EXAMPLES</span></span>

### <span data-ttu-id="3cb8a-114">Przykład 1: aktualizowanie bazy danych do standardowej bazy danych S0</span><span class="sxs-lookup"><span data-stu-id="3cb8a-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="3cb8a-115">To polecenie aktualizuje bazę danych o nazwie Database01 do standardowej bazy danych S0 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="3cb8a-116">Przykład 2: Dodawanie bazy danych do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="3cb8a-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="3cb8a-117">To polecenie dodaje bazę danych o nazwie Database01 do puli elastycznej o nazwie ElasticPool01 hostowanej na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="3cb8a-118">Przykład 3: modyfikowanie maksymalnego rozmiaru przestrzeni dyskowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="3cb8a-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="3cb8a-119">To polecenie aktualizuje bazę danych o nazwie Database01, aby ustawić jej maksymalny rozmiar na 1 TB.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="3cb8a-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cb8a-120">PARAMETERS</span></span>

### <span data-ttu-id="3cb8a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cb8a-121">-AsJob</span></span>
<span data-ttu-id="3cb8a-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3cb8a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cb8a-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="3cb8a-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="3cb8a-124">Opóźnienie automatycznego wstrzymania w minutach dla bazy danych (tylko na serwerze),-1 w celu rezygnacji</span><span class="sxs-lookup"><span data-stu-id="3cb8a-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="3cb8a-125">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="3cb8a-125">-BackupStorageRedundancy</span></span>
<span data-ttu-id="3cb8a-126">Nadmiarowość miejsca do magazynowania kopii zapasowej używana do przechowywania kopii zapasowych bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-126">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="3cb8a-127">Dostępne opcje: local, Zone i geo.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-127">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="3cb8a-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3cb8a-128">-ComputeGeneration</span></span>
<span data-ttu-id="3cb8a-129">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="3cb8a-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="3cb8a-130">-ComputeModel</span></span>
<span data-ttu-id="3cb8a-131">Obliczony model bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-131">Computed model of Azure Sql database.</span></span> <span data-ttu-id="3cb8a-132">Serwer lub Zainicjowano obsługę administracyjną</span><span class="sxs-lookup"><span data-stu-id="3cb8a-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="3cb8a-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3cb8a-133">-DatabaseName</span></span>
<span data-ttu-id="3cb8a-134">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3cb8a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb8a-135">-DefaultProfile</span></span>
<span data-ttu-id="3cb8a-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3cb8a-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cb8a-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="3cb8a-137">-Edition</span></span>
<span data-ttu-id="3cb8a-138">Określa wersję bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-138">Specifies the edition for the database.</span></span>
<span data-ttu-id="3cb8a-139">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3cb8a-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3cb8a-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3cb8a-140">None</span></span>
- <span data-ttu-id="3cb8a-141">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="3cb8a-141">Basic</span></span>
- <span data-ttu-id="3cb8a-142">Standard</span><span class="sxs-lookup"><span data-stu-id="3cb8a-142">Standard</span></span>
- <span data-ttu-id="3cb8a-143">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="3cb8a-143">Premium</span></span>
- <span data-ttu-id="3cb8a-144">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="3cb8a-144">DataWarehouse</span></span>
- <span data-ttu-id="3cb8a-145">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="3cb8a-145">Free</span></span>
- <span data-ttu-id="3cb8a-146">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="3cb8a-146">Stretch</span></span>
- <span data-ttu-id="3cb8a-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="3cb8a-147">GeneralPurpose</span></span>
- <span data-ttu-id="3cb8a-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="3cb8a-148">BusinessCritical</span></span>

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

### <span data-ttu-id="3cb8a-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3cb8a-149">-ElasticPoolName</span></span>
<span data-ttu-id="3cb8a-150">Określa nazwę puli elastycznej, w której ma zostać przeniesiona baza danych.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-150">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="3cb8a-151">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3cb8a-151">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="3cb8a-152">Liczba replik pomocniczych tylko do odczytu skojarzonych z bazą danych.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-152">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="3cb8a-153">Dotyczy tylko wersji z podskalą.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-153">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="3cb8a-154">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3cb8a-154">-LicenseType</span></span>
<span data-ttu-id="3cb8a-155">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-155">The license type for the Azure Sql database.</span></span> <span data-ttu-id="3cb8a-156">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="3cb8a-156">Possible values are:</span></span>
- <span data-ttu-id="3cb8a-157">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-157">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3cb8a-158">Cena bazy danych zostanie obniżona o istniejące właściciele licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-158">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3cb8a-159">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-159">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3cb8a-160">Cena bazy danych będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-160">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="3cb8a-161">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="3cb8a-161">-MaxSizeBytes</span></span>
<span data-ttu-id="3cb8a-162">Maksymalny rozmiar bazy danych SQL Azure w bajtach.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-162">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="3cb8a-163">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="3cb8a-163">-MinimumCapacity</span></span>
<span data-ttu-id="3cb8a-164">Minimalna pojemność bazy danych jest zawsze przydzielona, jeśli nie została wstrzymana.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-164">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="3cb8a-165">W przypadku baz danych platformy Azure SQL bezserwerowych.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-165">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="3cb8a-166">-NewName</span><span class="sxs-lookup"><span data-stu-id="3cb8a-166">-NewName</span></span>
<span data-ttu-id="3cb8a-167">Nowa nazwa, do której ma zostać zmieniona baza danych.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-167">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="3cb8a-168">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="3cb8a-168">-ReadScale</span></span>
<span data-ttu-id="3cb8a-169">Jeśli ta opcja jest włączona, połączenia z zastosowanymi aplikacjami, które mają ustawioną wartość tylko do odczytu, mogą być przekierowywane do repliki pomocniczej tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-169">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="3cb8a-170">Ta właściwość jest tylko do settable dla kluczowych baz danych Premium i dla firm.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-170">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="3cb8a-171">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="3cb8a-171">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="3cb8a-172">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-172">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="3cb8a-173">Aby uzyskać informacje na temat celów usługi, zobacz [warstwy usług Azure SQL Database i poziomy wydajności](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-173">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="3cb8a-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb8a-174">-ResourceGroupName</span></span>
<span data-ttu-id="3cb8a-175">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-175">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3cb8a-176">-Drugorzędny</span><span class="sxs-lookup"><span data-stu-id="3cb8a-176">-SecondaryType</span></span>
<span data-ttu-id="3cb8a-177">Pomocniczy typ bazy danych, jeśli jest pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-177">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="3cb8a-178">Prawidłowe wartości to Geo i Named.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-178">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="3cb8a-179">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3cb8a-179">-ServerName</span></span>
<span data-ttu-id="3cb8a-180">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-180">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3cb8a-181">-Tagi</span><span class="sxs-lookup"><span data-stu-id="3cb8a-181">-Tags</span></span>
<span data-ttu-id="3cb8a-182">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-182">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3cb8a-183">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="3cb8a-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3cb8a-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="3cb8a-184">-VCore</span></span>
<span data-ttu-id="3cb8a-185">Numer vCore bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3cb8a-185">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="3cb8a-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="3cb8a-186">-ZoneRedundant</span></span>
<span data-ttu-id="3cb8a-187">Nadmiarowość strefy do skojarzenia z bazą danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3cb8a-187">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="3cb8a-188">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3cb8a-188">-Confirm</span></span>
<span data-ttu-id="3cb8a-189">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb8a-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb8a-190">-WhatIf</span></span>
<span data-ttu-id="3cb8a-191">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb8a-192">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cb8a-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb8a-193">CommonParameters</span></span>
<span data-ttu-id="3cb8a-194">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb8a-195">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cb8a-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb8a-196">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cb8a-196">INPUTS</span></span>

### <span data-ttu-id="3cb8a-197">System. String</span><span class="sxs-lookup"><span data-stu-id="3cb8a-197">System.String</span></span>

## <span data-ttu-id="3cb8a-198">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cb8a-198">OUTPUTS</span></span>

### <span data-ttu-id="3cb8a-199">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3cb8a-199">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="3cb8a-200">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cb8a-200">NOTES</span></span>

## <span data-ttu-id="3cb8a-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cb8a-201">RELATED LINKS</span></span>

[<span data-ttu-id="3cb8a-202">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3cb8a-202">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="3cb8a-203">Nowe — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3cb8a-203">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="3cb8a-204">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3cb8a-204">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="3cb8a-205">Życiorys — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3cb8a-205">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="3cb8a-206">Suspend — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3cb8a-206">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="3cb8a-207">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3cb8a-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
