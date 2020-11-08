---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 180cd3c8d9301ab287bc4a37c13f7b07276f7794
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049837"
---
# <span data-ttu-id="72c7d-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="72c7d-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="72c7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="72c7d-103">Ustawia właściwości bazy danych lub przenosi istniejącą bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="72c7d-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="72c7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72c7d-104">SYNTAX</span></span>

### <span data-ttu-id="72c7d-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="72c7d-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c7d-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="72c7d-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c7d-107">Nazwy</span><span class="sxs-lookup"><span data-stu-id="72c7d-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72c7d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="72c7d-108">DESCRIPTION</span></span>
<span data-ttu-id="72c7d-109">Polecenie cmdlet **Set-AzSqlDatabase** ustawia właściwości bazy danych w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="72c7d-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="72c7d-110">To polecenie cmdlet może zmodyfikować warstwę usług ( *wersja* ), poziom wydajności ( *RequestedServiceObjectiveName* ) i maksymalny rozmiar magazynu ( *MaxSizeBytes* ) bazy danych.</span><span class="sxs-lookup"><span data-stu-id="72c7d-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="72c7d-111">Ponadto można określić parametr *ElasticPoolName* , aby przenieść bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="72c7d-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="72c7d-112">Jeśli baza danych znajduje się już w puli elastycznej, można użyć parametru *RequestedServiceObjectiveName* , aby przenieść bazę danych poza elastyczną pulę i na poziom wydajności dla pojedynczych baz danych.</span><span class="sxs-lookup"><span data-stu-id="72c7d-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="72c7d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72c7d-113">EXAMPLES</span></span>

### <span data-ttu-id="72c7d-114">Przykład 1: aktualizowanie bazy danych do standardowej bazy danych S0</span><span class="sxs-lookup"><span data-stu-id="72c7d-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="72c7d-115">To polecenie aktualizuje bazę danych o nazwie Database01 do standardowej bazy danych S0 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="72c7d-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="72c7d-116">Przykład 2: Dodawanie bazy danych do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="72c7d-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="72c7d-117">To polecenie dodaje bazę danych o nazwie Database01 do puli elastycznej o nazwie ElasticPool01 hostowanej na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="72c7d-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="72c7d-118">Przykład 3: modyfikowanie maksymalnego rozmiaru przestrzeni dyskowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="72c7d-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="72c7d-119">To polecenie aktualizuje bazę danych o nazwie Database01, aby ustawić jej maksymalny rozmiar na 1 TB.</span><span class="sxs-lookup"><span data-stu-id="72c7d-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="72c7d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72c7d-120">PARAMETERS</span></span>

### <span data-ttu-id="72c7d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72c7d-121">-AsJob</span></span>
<span data-ttu-id="72c7d-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="72c7d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72c7d-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="72c7d-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="72c7d-124">Opóźnienie automatycznego wstrzymania w minutach dla bazy danych (tylko na serwerze),-1 w celu rezygnacji</span><span class="sxs-lookup"><span data-stu-id="72c7d-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="72c7d-125">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="72c7d-125">-ComputeGeneration</span></span>
<span data-ttu-id="72c7d-126">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="72c7d-126">The compute generation to assign.</span></span>

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

### <span data-ttu-id="72c7d-127">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="72c7d-127">-ComputeModel</span></span>
<span data-ttu-id="72c7d-128">Obliczony model bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="72c7d-128">Computed model of Azure Sql database.</span></span> <span data-ttu-id="72c7d-129">Serwer lub Zainicjowano obsługę administracyjną</span><span class="sxs-lookup"><span data-stu-id="72c7d-129">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="72c7d-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="72c7d-130">-DatabaseName</span></span>
<span data-ttu-id="72c7d-131">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="72c7d-131">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="72c7d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c7d-132">-DefaultProfile</span></span>
<span data-ttu-id="72c7d-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="72c7d-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72c7d-134">-Edition</span><span class="sxs-lookup"><span data-stu-id="72c7d-134">-Edition</span></span>
<span data-ttu-id="72c7d-135">Określa wersję bazy danych.</span><span class="sxs-lookup"><span data-stu-id="72c7d-135">Specifies the edition for the database.</span></span>
<span data-ttu-id="72c7d-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="72c7d-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72c7d-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="72c7d-137">None</span></span>
- <span data-ttu-id="72c7d-138">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="72c7d-138">Basic</span></span>
- <span data-ttu-id="72c7d-139">Standard</span><span class="sxs-lookup"><span data-stu-id="72c7d-139">Standard</span></span>
- <span data-ttu-id="72c7d-140">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="72c7d-140">Premium</span></span>
- <span data-ttu-id="72c7d-141">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="72c7d-141">DataWarehouse</span></span>
- <span data-ttu-id="72c7d-142">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="72c7d-142">Free</span></span>
- <span data-ttu-id="72c7d-143">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="72c7d-143">Stretch</span></span>
- <span data-ttu-id="72c7d-144">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="72c7d-144">GeneralPurpose</span></span>
- <span data-ttu-id="72c7d-145">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="72c7d-145">BusinessCritical</span></span>

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

### <span data-ttu-id="72c7d-146">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="72c7d-146">-ElasticPoolName</span></span>
<span data-ttu-id="72c7d-147">Określa nazwę puli elastycznej, w której ma zostać przeniesiona baza danych.</span><span class="sxs-lookup"><span data-stu-id="72c7d-147">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="72c7d-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="72c7d-148">-LicenseType</span></span>
<span data-ttu-id="72c7d-149">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="72c7d-149">The license type for the Azure Sql database.</span></span> <span data-ttu-id="72c7d-150">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="72c7d-150">Possible values are:</span></span>
- <span data-ttu-id="72c7d-151">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72c7d-151">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="72c7d-152">Cena bazy danych zostanie obniżona o istniejące właściciele licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72c7d-152">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="72c7d-153">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="72c7d-153">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="72c7d-154">Cena bazy danych będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72c7d-154">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="72c7d-155">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="72c7d-155">-MaxSizeBytes</span></span>
<span data-ttu-id="72c7d-156">Maksymalny rozmiar bazy danych SQL Azure w bajtach.</span><span class="sxs-lookup"><span data-stu-id="72c7d-156">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="72c7d-157">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="72c7d-157">-MinimumCapacity</span></span>
<span data-ttu-id="72c7d-158">Minimalna pojemność bazy danych jest zawsze przydzielona, jeśli nie została wstrzymana.</span><span class="sxs-lookup"><span data-stu-id="72c7d-158">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="72c7d-159">W przypadku baz danych platformy Azure SQL bezserwerowych.</span><span class="sxs-lookup"><span data-stu-id="72c7d-159">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="72c7d-160">-NewName</span><span class="sxs-lookup"><span data-stu-id="72c7d-160">-NewName</span></span>
<span data-ttu-id="72c7d-161">Nowa nazwa, do której ma zostać zmieniona baza danych.</span><span class="sxs-lookup"><span data-stu-id="72c7d-161">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="72c7d-162">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="72c7d-162">-ReadReplicaCount</span></span>
<span data-ttu-id="72c7d-163">Liczba replik pomocniczych tylko do odczytu skojarzonych z bazą danych.</span><span class="sxs-lookup"><span data-stu-id="72c7d-163">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="72c7d-164">Dotyczy tylko wersji z podskalą.</span><span class="sxs-lookup"><span data-stu-id="72c7d-164">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="72c7d-165">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="72c7d-165">-ReadScale</span></span>
<span data-ttu-id="72c7d-166">Jeśli ta opcja jest włączona, połączenia z zastosowanymi aplikacjami, które mają ustawioną wartość tylko do odczytu, mogą być przekierowywane do repliki pomocniczej tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="72c7d-166">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="72c7d-167">Ta właściwość jest tylko do settable dla kluczowych baz danych Premium i dla firm.</span><span class="sxs-lookup"><span data-stu-id="72c7d-167">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="72c7d-168">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="72c7d-168">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="72c7d-169">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="72c7d-169">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="72c7d-170">Aby uzyskać informacje na temat celów usługi, zobacz [warstwy usług Azure SQL Database i poziomy wydajności](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="72c7d-170">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="72c7d-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c7d-171">-ResourceGroupName</span></span>
<span data-ttu-id="72c7d-172">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="72c7d-172">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="72c7d-173">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="72c7d-173">-ServerName</span></span>
<span data-ttu-id="72c7d-174">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="72c7d-174">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="72c7d-175">-Tagi</span><span class="sxs-lookup"><span data-stu-id="72c7d-175">-Tags</span></span>
<span data-ttu-id="72c7d-176">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="72c7d-176">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="72c7d-177">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="72c7d-177">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="72c7d-178">-VCore</span><span class="sxs-lookup"><span data-stu-id="72c7d-178">-VCore</span></span>
<span data-ttu-id="72c7d-179">Numer vCore bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="72c7d-179">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="72c7d-180">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="72c7d-180">-ZoneRedundant</span></span>
<span data-ttu-id="72c7d-181">Nadmiarowość strefy do skojarzenia z bazą danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="72c7d-181">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="72c7d-182">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72c7d-182">-Confirm</span></span>
<span data-ttu-id="72c7d-183">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72c7d-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72c7d-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72c7d-184">-WhatIf</span></span>
<span data-ttu-id="72c7d-185">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72c7d-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72c7d-186">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72c7d-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72c7d-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c7d-187">CommonParameters</span></span>
<span data-ttu-id="72c7d-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c7d-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c7d-189">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72c7d-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c7d-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72c7d-190">INPUTS</span></span>

### <span data-ttu-id="72c7d-191">System. String</span><span class="sxs-lookup"><span data-stu-id="72c7d-191">System.String</span></span>

## <span data-ttu-id="72c7d-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72c7d-192">OUTPUTS</span></span>

### <span data-ttu-id="72c7d-193">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="72c7d-193">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="72c7d-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72c7d-194">NOTES</span></span>

## <span data-ttu-id="72c7d-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72c7d-195">RELATED LINKS</span></span>

[<span data-ttu-id="72c7d-196">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="72c7d-196">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="72c7d-197">Nowe — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="72c7d-197">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="72c7d-198">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="72c7d-198">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="72c7d-199">Życiorys — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="72c7d-199">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="72c7d-200">Suspend — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="72c7d-200">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="72c7d-201">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="72c7d-201">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
