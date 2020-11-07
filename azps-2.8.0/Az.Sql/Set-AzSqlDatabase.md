---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: dd69e345e5e2bac5ebab0ec4e45c03501ccc8139
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887281"
---
# <span data-ttu-id="531bf-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="531bf-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="531bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="531bf-102">SYNOPSIS</span></span>
<span data-ttu-id="531bf-103">Ustawia właściwości bazy danych lub przenosi istniejącą bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="531bf-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="531bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="531bf-104">SYNTAX</span></span>

### <span data-ttu-id="531bf-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="531bf-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="531bf-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="531bf-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="531bf-107">Nazwy</span><span class="sxs-lookup"><span data-stu-id="531bf-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="531bf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="531bf-108">DESCRIPTION</span></span>
<span data-ttu-id="531bf-109">Polecenie cmdlet **Set-AzSqlDatabase** ustawia właściwości bazy danych w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="531bf-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="531bf-110">To polecenie cmdlet może zmodyfikować warstwę usług ( *wersja* ), poziom wydajności ( *RequestedServiceObjectiveName* ) i maksymalny rozmiar magazynu ( *MaxSizeBytes* ) bazy danych.</span><span class="sxs-lookup"><span data-stu-id="531bf-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="531bf-111">Ponadto można określić parametr *ElasticPoolName* , aby przenieść bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="531bf-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="531bf-112">Jeśli baza danych znajduje się już w puli elastycznej, można użyć parametru *RequestedServiceObjectiveName* , aby przenieść bazę danych poza elastyczną pulę i na poziom wydajności dla pojedynczych baz danych.</span><span class="sxs-lookup"><span data-stu-id="531bf-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="531bf-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="531bf-113">EXAMPLES</span></span>

### <span data-ttu-id="531bf-114">Przykład 1: aktualizowanie bazy danych do standardowej bazy danych S0</span><span class="sxs-lookup"><span data-stu-id="531bf-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="531bf-115">To polecenie aktualizuje bazę danych o nazwie Database01 do standardowej bazy danych S0 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="531bf-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="531bf-116">Przykład 2: Dodawanie bazy danych do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="531bf-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="531bf-117">To polecenie dodaje bazę danych o nazwie Database01 do puli elastycznej o nazwie ElasticPool01 hostowanej na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="531bf-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="531bf-118">Przykład 3: modyfikowanie maksymalnego rozmiaru przestrzeni dyskowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="531bf-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="531bf-119">To polecenie aktualizuje bazę danych o nazwie Database01, aby ustawić jej maksymalny rozmiar na 1 TB.</span><span class="sxs-lookup"><span data-stu-id="531bf-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="531bf-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="531bf-120">PARAMETERS</span></span>

### <span data-ttu-id="531bf-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="531bf-121">-AsJob</span></span>
<span data-ttu-id="531bf-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="531bf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="531bf-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="531bf-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="531bf-124">Opóźnienie automatycznego wstrzymania w minutach dla bazy danych (tylko na serwerze),-1 w celu rezygnacji</span><span class="sxs-lookup"><span data-stu-id="531bf-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="531bf-125">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="531bf-125">-ComputeGeneration</span></span>
<span data-ttu-id="531bf-126">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="531bf-126">The compute generation to assign.</span></span>

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

### <span data-ttu-id="531bf-127">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="531bf-127">-ComputeModel</span></span>
<span data-ttu-id="531bf-128">Obliczony model bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="531bf-128">Computed model of Azure Sql database.</span></span> <span data-ttu-id="531bf-129">Serwer lub Zainicjowano obsługę administracyjną</span><span class="sxs-lookup"><span data-stu-id="531bf-129">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="531bf-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="531bf-130">-DatabaseName</span></span>
<span data-ttu-id="531bf-131">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="531bf-131">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="531bf-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531bf-132">-DefaultProfile</span></span>
<span data-ttu-id="531bf-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="531bf-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="531bf-134">-Edition</span><span class="sxs-lookup"><span data-stu-id="531bf-134">-Edition</span></span>
<span data-ttu-id="531bf-135">Określa wersję bazy danych.</span><span class="sxs-lookup"><span data-stu-id="531bf-135">Specifies the edition for the database.</span></span>
<span data-ttu-id="531bf-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="531bf-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="531bf-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="531bf-137">None</span></span>
- <span data-ttu-id="531bf-138">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="531bf-138">Basic</span></span>
- <span data-ttu-id="531bf-139">Standard</span><span class="sxs-lookup"><span data-stu-id="531bf-139">Standard</span></span>
- <span data-ttu-id="531bf-140">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="531bf-140">Premium</span></span>
- <span data-ttu-id="531bf-141">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="531bf-141">DataWarehouse</span></span>
- <span data-ttu-id="531bf-142">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="531bf-142">Free</span></span>
- <span data-ttu-id="531bf-143">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="531bf-143">Stretch</span></span>
- <span data-ttu-id="531bf-144">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="531bf-144">GeneralPurpose</span></span>
- <span data-ttu-id="531bf-145">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="531bf-145">BusinessCritical</span></span>

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

### <span data-ttu-id="531bf-146">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="531bf-146">-ElasticPoolName</span></span>
<span data-ttu-id="531bf-147">Określa nazwę puli elastycznej, w której ma zostać przeniesiona baza danych.</span><span class="sxs-lookup"><span data-stu-id="531bf-147">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="531bf-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="531bf-148">-LicenseType</span></span>
<span data-ttu-id="531bf-149">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="531bf-149">The license type for the Azure Sql database.</span></span> <span data-ttu-id="531bf-150">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="531bf-150">Possible values are:</span></span>
- <span data-ttu-id="531bf-151">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="531bf-151">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="531bf-152">Cena bazy danych zostanie obniżona o istniejące właściciele licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="531bf-152">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="531bf-153">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="531bf-153">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="531bf-154">Cena bazy danych będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="531bf-154">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="531bf-155">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="531bf-155">-MaxSizeBytes</span></span>
<span data-ttu-id="531bf-156">Maksymalny rozmiar bazy danych SQL Azure w bajtach.</span><span class="sxs-lookup"><span data-stu-id="531bf-156">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="531bf-157">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="531bf-157">-MinimumCapacity</span></span>
<span data-ttu-id="531bf-158">Minimalna pojemność bazy danych jest zawsze przydzielona, jeśli nie została wstrzymana.</span><span class="sxs-lookup"><span data-stu-id="531bf-158">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="531bf-159">W przypadku baz danych platformy Azure SQL bezserwerowych.</span><span class="sxs-lookup"><span data-stu-id="531bf-159">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531bf-160">-NewName</span><span class="sxs-lookup"><span data-stu-id="531bf-160">-NewName</span></span>
<span data-ttu-id="531bf-161">Nowa nazwa, do której ma zostać zmieniona baza danych.</span><span class="sxs-lookup"><span data-stu-id="531bf-161">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="531bf-162">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="531bf-162">-ReadScale</span></span>
<span data-ttu-id="531bf-163">Opcja Skala odczytu umożliwiająca przypisanie do bazy danych SQL Azure. (Włączone/wyłączone)</span><span class="sxs-lookup"><span data-stu-id="531bf-163">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="531bf-164">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="531bf-164">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="531bf-165">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="531bf-165">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="531bf-166">Aby uzyskać informacje na temat celów usługi, zobacz [warstwy usług Azure SQL Database i poziomy wydajności](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="531bf-166">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="531bf-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="531bf-167">-ResourceGroupName</span></span>
<span data-ttu-id="531bf-168">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="531bf-168">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="531bf-169">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="531bf-169">-ServerName</span></span>
<span data-ttu-id="531bf-170">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="531bf-170">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="531bf-171">-Tagi</span><span class="sxs-lookup"><span data-stu-id="531bf-171">-Tags</span></span>
<span data-ttu-id="531bf-172">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="531bf-172">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="531bf-173">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="531bf-173">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="531bf-174">-VCore</span><span class="sxs-lookup"><span data-stu-id="531bf-174">-VCore</span></span>
<span data-ttu-id="531bf-175">Numer vCore bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="531bf-175">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="531bf-176">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="531bf-176">-ZoneRedundant</span></span>
<span data-ttu-id="531bf-177">Nadmiarowość strefy do skojarzenia z bazą danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="531bf-177">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="531bf-178">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="531bf-178">-Confirm</span></span>
<span data-ttu-id="531bf-179">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="531bf-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="531bf-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="531bf-180">-WhatIf</span></span>
<span data-ttu-id="531bf-181">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="531bf-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="531bf-182">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="531bf-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="531bf-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531bf-183">CommonParameters</span></span>
<span data-ttu-id="531bf-184">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="531bf-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531bf-185">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="531bf-185">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531bf-186">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="531bf-186">INPUTS</span></span>

### <span data-ttu-id="531bf-187">System. String</span><span class="sxs-lookup"><span data-stu-id="531bf-187">System.String</span></span>

## <span data-ttu-id="531bf-188">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="531bf-188">OUTPUTS</span></span>

### <span data-ttu-id="531bf-189">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="531bf-189">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="531bf-190">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="531bf-190">NOTES</span></span>

## <span data-ttu-id="531bf-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="531bf-191">RELATED LINKS</span></span>

[<span data-ttu-id="531bf-192">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="531bf-192">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="531bf-193">Nowe — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="531bf-193">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="531bf-194">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="531bf-194">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="531bf-195">Życiorys — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="531bf-195">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="531bf-196">Suspend — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="531bf-196">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="531bf-197">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="531bf-197">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
