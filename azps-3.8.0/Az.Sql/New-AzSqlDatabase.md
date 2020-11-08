---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 32329ac1e36c74c08dcf25f8f8b4295e81633e90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049718"
---
# <span data-ttu-id="fddb3-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fddb3-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="fddb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fddb3-102">SYNOPSIS</span></span>
<span data-ttu-id="fddb3-103">Tworzy bazę danych lub elastyczną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="fddb3-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="fddb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fddb3-104">SYNTAX</span></span>

### <span data-ttu-id="fddb3-105">DtuBasedDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fddb3-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fddb3-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="fddb3-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fddb3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fddb3-107">DESCRIPTION</span></span>
<span data-ttu-id="fddb3-108">Polecenie cmdlet **New-AzSqlDatabase** tworzy bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fddb3-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="fddb3-109">Możesz również utworzyć elastyczną bazę danych, ustawiając parametr *ElasticPoolName* na istniejącą pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="fddb3-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="fddb3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fddb3-110">EXAMPLES</span></span>

### <span data-ttu-id="fddb3-111">Przykład 1: Tworzenie bazy danych na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="fddb3-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="fddb3-112">To polecenie tworzy bazę danych o nazwie Database01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="fddb3-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="fddb3-113">Przykład 2: Tworzenie Elastic Database na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="fddb3-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="fddb3-114">To polecenie tworzy bazę danych o nazwie Database02 w puli elastycznej o nazwie ElasticPool01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="fddb3-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="fddb3-115">Przykład 3: Tworzenie bazy danych programu vCore na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="fddb3-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="fddb3-116">To polecenie tworzy bazę danych vCore o nazwie Database03 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="fddb3-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="fddb3-117">Przykład 4: Tworzenie bazy danych serwera na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="fddb3-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="fddb3-118">To polecenie tworzy bezserwerową bazę danych o nazwie Database04 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="fddb3-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="fddb3-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fddb3-119">PARAMETERS</span></span>

### <span data-ttu-id="fddb3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fddb3-120">-AsJob</span></span>
<span data-ttu-id="fddb3-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fddb3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fddb3-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="fddb3-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="fddb3-123">Opóźnienie automatycznego wstrzymania w minutach dla bazy danych (tylko na serwerze),-1 w celu rezygnacji</span><span class="sxs-lookup"><span data-stu-id="fddb3-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-124">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="fddb3-124">-CatalogCollation</span></span>
<span data-ttu-id="fddb3-125">Określa nazwę sortowania wykazu bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="fddb3-125">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="fddb3-126">-CollationName</span><span class="sxs-lookup"><span data-stu-id="fddb3-126">-CollationName</span></span>
<span data-ttu-id="fddb3-127">Określa nazwę sortowania bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="fddb3-127">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="fddb3-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="fddb3-128">-ComputeGeneration</span></span>
<span data-ttu-id="fddb3-129">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="fddb3-129">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="fddb3-130">-ComputeModel</span></span>
<span data-ttu-id="fddb3-131">Model obliczeniowy dla bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="fddb3-131">The compute model for Azure Sql database.</span></span> <span data-ttu-id="fddb3-132">Serwer lub Zainicjowano obsługę administracyjną</span><span class="sxs-lookup"><span data-stu-id="fddb3-132">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fddb3-133">-DatabaseName</span></span>
<span data-ttu-id="fddb3-134">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fddb3-134">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddb3-135">-DefaultProfile</span></span>
<span data-ttu-id="fddb3-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fddb3-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fddb3-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="fddb3-137">-Edition</span></span>
<span data-ttu-id="fddb3-138">Określa wydanie, które ma zostać przypisane do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fddb3-138">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="fddb3-139">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fddb3-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fddb3-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fddb3-140">None</span></span>
- <span data-ttu-id="fddb3-141">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="fddb3-141">Basic</span></span>
- <span data-ttu-id="fddb3-142">Standard</span><span class="sxs-lookup"><span data-stu-id="fddb3-142">Standard</span></span>
- <span data-ttu-id="fddb3-143">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="fddb3-143">Premium</span></span>
- <span data-ttu-id="fddb3-144">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="fddb3-144">DataWarehouse</span></span>
- <span data-ttu-id="fddb3-145">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="fddb3-145">Free</span></span>
- <span data-ttu-id="fddb3-146">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="fddb3-146">Stretch</span></span>
- <span data-ttu-id="fddb3-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="fddb3-147">GeneralPurpose</span></span>
- <span data-ttu-id="fddb3-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="fddb3-148">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fddb3-149">-ElasticPoolName</span></span>
<span data-ttu-id="fddb3-150">Określa nazwę puli elastycznej, w której ma zostać umieszczona baza danych.</span><span class="sxs-lookup"><span data-stu-id="fddb3-150">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fddb3-151">-LicenseType</span></span>
<span data-ttu-id="fddb3-152">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fddb3-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="fddb3-153">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="fddb3-153">Possible values are:</span></span>
- <span data-ttu-id="fddb3-154">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fddb3-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="fddb3-155">Cena bazy danych zostanie obniżona o istniejące właściciele licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fddb3-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="fddb3-156">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="fddb3-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="fddb3-157">Cena bazy danych będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fddb3-157">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="fddb3-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="fddb3-158">-MaxSizeBytes</span></span>
<span data-ttu-id="fddb3-159">Określa maksymalny rozmiar bazy danych w bajtach.</span><span class="sxs-lookup"><span data-stu-id="fddb3-159">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-160">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="fddb3-160">-MinimumCapacity</span></span>
<span data-ttu-id="fddb3-161">Minimalna pojemność bazy danych jest zawsze przydzielona, jeśli nie została wstrzymana.</span><span class="sxs-lookup"><span data-stu-id="fddb3-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="fddb3-162">W przypadku baz danych platformy Azure SQL bezserwerowych.</span><span class="sxs-lookup"><span data-stu-id="fddb3-162">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-163">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="fddb3-163">-ReadReplicaCount</span></span>
<span data-ttu-id="fddb3-164">Liczba replik pomocniczych tylko do odczytu skojarzonych z bazą danych, do której mogą być przekierowywane połączenia z przeznaczeniem aplikacji tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="fddb3-164">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="fddb3-165">Ta właściwość jest dostępna tylko w przypadku baz danych z podskalą wersji.</span><span class="sxs-lookup"><span data-stu-id="fddb3-165">This property is only settable for Hyperscale edition databases.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-166">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="fddb3-166">-ReadScale</span></span>
<span data-ttu-id="fddb3-167">Jeśli ta opcja jest włączona, połączenia z zastosowanymi aplikacjami, które mają ustawioną wartość tylko do odczytu, mogą być przekierowywane do repliki pomocniczej tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="fddb3-167">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="fddb3-168">Ta właściwość jest tylko do settable dla kluczowych baz danych Premium i dla firm.</span><span class="sxs-lookup"><span data-stu-id="fddb3-168">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-169">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="fddb3-169">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="fddb3-170">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fddb3-170">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fddb3-171">-ResourceGroupName</span></span>
<span data-ttu-id="fddb3-172">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="fddb3-172">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fddb3-173">-Samplename</span><span class="sxs-lookup"><span data-stu-id="fddb3-173">-SampleName</span></span>
<span data-ttu-id="fddb3-174">Nazwa przykładowego schematu, który ma zostać zastosowany podczas tworzenia tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fddb3-174">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-175">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fddb3-175">-ServerName</span></span>
<span data-ttu-id="fddb3-176">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="fddb3-176">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="fddb3-177">-Tagi</span><span class="sxs-lookup"><span data-stu-id="fddb3-177">-Tags</span></span>
<span data-ttu-id="fddb3-178">Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z nową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="fddb3-178">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="fddb3-179">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="fddb3-179">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-180">-VCore</span><span class="sxs-lookup"><span data-stu-id="fddb3-180">-VCore</span></span>
<span data-ttu-id="fddb3-181">Numer vCore bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="fddb3-181">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddb3-182">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="fddb3-182">-ZoneRedundant</span></span>
<span data-ttu-id="fddb3-183">Nadmiarowość strefy do skojarzenia z bazą danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="fddb3-183">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="fddb3-184">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fddb3-184">-Confirm</span></span>
<span data-ttu-id="fddb3-185">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fddb3-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fddb3-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fddb3-186">-WhatIf</span></span>
<span data-ttu-id="fddb3-187">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fddb3-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fddb3-188">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fddb3-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fddb3-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fddb3-189">CommonParameters</span></span>
<span data-ttu-id="fddb3-190">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fddb3-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fddb3-191">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fddb3-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fddb3-192">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fddb3-192">INPUTS</span></span>

### <span data-ttu-id="fddb3-193">System. String</span><span class="sxs-lookup"><span data-stu-id="fddb3-193">System.String</span></span>

## <span data-ttu-id="fddb3-194">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fddb3-194">OUTPUTS</span></span>

### <span data-ttu-id="fddb3-195">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fddb3-195">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fddb3-196">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fddb3-196">NOTES</span></span>

## <span data-ttu-id="fddb3-197">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fddb3-197">RELATED LINKS</span></span>

[<span data-ttu-id="fddb3-198">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fddb3-198">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="fddb3-199">Nowe — AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fddb3-199">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="fddb3-200">Nowe — AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="fddb3-200">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="fddb3-201">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fddb3-201">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="fddb3-202">Życiorys — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fddb3-202">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="fddb3-203">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fddb3-203">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="fddb3-204">Suspend — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fddb3-204">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="fddb3-205">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fddb3-205">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

