---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: c4ccb57292fd4abc2c9b6fd14c5e4492047a2e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956593"
---
# <span data-ttu-id="b8838-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8838-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="b8838-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8838-102">SYNOPSIS</span></span>
<span data-ttu-id="b8838-103">Tworzy bazę danych lub elastyczną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="b8838-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="b8838-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8838-104">SYNTAX</span></span>

### <span data-ttu-id="b8838-105">DtuBasedDatabase (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b8838-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8838-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="b8838-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8838-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8838-107">DESCRIPTION</span></span>
<span data-ttu-id="b8838-108">Polecenie **cmdlet New-AzSqlDatabase** tworzy bazę danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b8838-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="b8838-109">Możesz również utworzyć elastyczną bazę danych, ustawiając parametr *1000111 na* istniejącą pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="b8838-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="b8838-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8838-110">EXAMPLES</span></span>

### <span data-ttu-id="b8838-111">Przykład 1. Tworzenie bazy danych na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="b8838-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="b8838-112">To polecenie tworzy bazę danych o nazwie Database01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="b8838-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="b8838-113">Przykład 2. Tworzenie elastycznej bazy danych na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="b8838-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="b8838-114">To polecenie tworzy bazę danych o nazwie Database02 w puli elastycznej o nazwie Chembojna Bufor01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="b8838-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="b8838-115">Przykład 3. Tworzenie bazy danych Vcore na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="b8838-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="b8838-116">To polecenie tworzy bazę danych Vcore o nazwie Database03 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="b8838-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="b8838-117">Przykład 4. Tworzenie bazy danych bez serwera na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="b8838-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="b8838-118">To polecenie tworzy niebędąc serwerem bazę danych o nazwie Database04 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="b8838-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="b8838-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8838-119">PARAMETERS</span></span>

### <span data-ttu-id="b8838-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b8838-120">-AsJob</span></span>
<span data-ttu-id="b8838-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b8838-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8838-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="b8838-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="b8838-123">Opóźnienie automatycznego wstrzymania w minutach w przypadku bazy danych(tylko bez serwera), -1 w celu rezygnacji</span><span class="sxs-lookup"><span data-stu-id="b8838-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="b8838-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="b8838-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="b8838-125">Nadmiarowość magazynu kopii zapasowej używana do przechowywania kopii zapasowych dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b8838-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="b8838-126">Dostępne są następujące opcje: Lokalny, Strefa i Geo.</span><span class="sxs-lookup"><span data-stu-id="b8838-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="b8838-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="b8838-127">-CatalogCollation</span></span>
<span data-ttu-id="b8838-128">Określa nazwę sortowania wykazu bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b8838-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="b8838-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="b8838-129">-CollationName</span></span>
<span data-ttu-id="b8838-130">Określa nazwę sortowania bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b8838-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="b8838-131">-Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="b8838-131">-ComputeGeneration</span></span>
<span data-ttu-id="b8838-132">Generowanie obliczeniowe do przypisania.</span><span class="sxs-lookup"><span data-stu-id="b8838-132">The compute generation to assign.</span></span>

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

### <span data-ttu-id="b8838-133">- ComputeModel</span><span class="sxs-lookup"><span data-stu-id="b8838-133">-ComputeModel</span></span>
<span data-ttu-id="b8838-134">Model obliczeniowy bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="b8838-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="b8838-135">Bez serwera lub z inicjowaniem obsługi administracyjnej</span><span class="sxs-lookup"><span data-stu-id="b8838-135">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="b8838-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8838-136">-DatabaseName</span></span>
<span data-ttu-id="b8838-137">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b8838-137">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="b8838-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8838-138">-DefaultProfile</span></span>
<span data-ttu-id="b8838-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b8838-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8838-140">— wersja</span><span class="sxs-lookup"><span data-stu-id="b8838-140">-Edition</span></span>
<span data-ttu-id="b8838-141">Określa wersję do przypisania do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b8838-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="b8838-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b8838-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8838-143">Brak</span><span class="sxs-lookup"><span data-stu-id="b8838-143">None</span></span>
- <span data-ttu-id="b8838-144">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="b8838-144">Basic</span></span>
- <span data-ttu-id="b8838-145">Standardowe</span><span class="sxs-lookup"><span data-stu-id="b8838-145">Standard</span></span>
- <span data-ttu-id="b8838-146">Premium</span><span class="sxs-lookup"><span data-stu-id="b8838-146">Premium</span></span>
- <span data-ttu-id="b8838-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="b8838-147">DataWarehouse</span></span>
- <span data-ttu-id="b8838-148">Bezpłatne</span><span class="sxs-lookup"><span data-stu-id="b8838-148">Free</span></span>
- <span data-ttu-id="b8838-149">Rozciągnięcie</span><span class="sxs-lookup"><span data-stu-id="b8838-149">Stretch</span></span>
- <span data-ttu-id="b8838-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="b8838-150">GeneralPurpose</span></span>
- <span data-ttu-id="b8838-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="b8838-151">BusinessCritical</span></span>

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

### <span data-ttu-id="b8838-152">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="b8838-152">-ElasticPoolName</span></span>
<span data-ttu-id="b8838-153">Określa nazwę puli elastycznej, w której ma być umieszczana baza danych.</span><span class="sxs-lookup"><span data-stu-id="b8838-153">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="b8838-154">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b8838-154">-Force</span></span>
<span data-ttu-id="b8838-155">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="b8838-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b8838-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="b8838-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="b8838-157">Liczba replik pomocniczych tylko do odczytu skojarzonych z bazą danych, do których mogą być kierowane tylko połączenia przez aplikację.</span><span class="sxs-lookup"><span data-stu-id="b8838-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="b8838-158">Tę właściwość można ustawiać tylko w przypadku baz danych w wersji Hyperscale.</span><span class="sxs-lookup"><span data-stu-id="b8838-158">This property is only settable for Hyperscale edition databases.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8838-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b8838-159">-LicenseType</span></span>
<span data-ttu-id="b8838-160">Typ licencji dla bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="b8838-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="b8838-161">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="b8838-161">Possible values are:</span></span>
- <span data-ttu-id="b8838-162">Cena Bazowa — zastosowano rabat w ramach korzyści hybrydowej platformy Azure (AHB) dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b8838-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="b8838-163">Cena bazy danych zostanie z rabatem dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b8838-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="b8838-164">Cena rabatu z rabatem na usługę Azure Hybrid Benefit (AHB) dla istniejących właścicieli licencji programu SQL Server nie jest stosowana.</span><span class="sxs-lookup"><span data-stu-id="b8838-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="b8838-165">Cena bazy danych będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b8838-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="b8838-166">- MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b8838-166">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="b8838-167">Identyfikator konfiguracji konserwacji bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b8838-167">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="b8838-168">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="b8838-168">-MaxSizeBytes</span></span>
<span data-ttu-id="b8838-169">Określa maksymalny rozmiar bazy danych (w bajtach).</span><span class="sxs-lookup"><span data-stu-id="b8838-169">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="b8838-170">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="b8838-170">-MinimumCapacity</span></span>
<span data-ttu-id="b8838-171">Minimalna pojemność, która będzie przydzielana przez bazę danych, jeśli nie zostanie wstrzymana.</span><span class="sxs-lookup"><span data-stu-id="b8838-171">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="b8838-172">Tylko bazy danych Azure Sql bez serwera.</span><span class="sxs-lookup"><span data-stu-id="b8838-172">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="b8838-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="b8838-173">-ReadScale</span></span>
<span data-ttu-id="b8838-174">Jeśli ta funkcja jest włączona, połączenia, dla których celem aplikacji ustawiono odczyt tylko do odczytu w ciągu połączenia, mogą być kierowane do repliki pomocniczej tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="b8838-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="b8838-175">Tę właściwość można ustawiać tylko w przypadku baz danych o krytycznym znaczeniu dla wersji Premium i Business.</span><span class="sxs-lookup"><span data-stu-id="b8838-175">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="b8838-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b8838-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="b8838-177">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b8838-177">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="b8838-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8838-178">-ResourceGroupName</span></span>
<span data-ttu-id="b8838-179">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="b8838-179">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b8838-180">-SampleName</span><span class="sxs-lookup"><span data-stu-id="b8838-180">-SampleName</span></span>
<span data-ttu-id="b8838-181">Nazwa przykładowego schematu do zastosowania podczas tworzenia tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b8838-181">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="b8838-182">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="b8838-182">-SecondaryType</span></span>
<span data-ttu-id="b8838-183">Pomocniczy typ bazy danych, jeśli jest to pomocniczy typ bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b8838-183">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="b8838-184">Prawidłowe wartości to Geo i Named.</span><span class="sxs-lookup"><span data-stu-id="b8838-184">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="b8838-185">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8838-185">-ServerName</span></span>
<span data-ttu-id="b8838-186">Określa nazwę serwera hostowego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="b8838-186">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b8838-187">— Tagi</span><span class="sxs-lookup"><span data-stu-id="b8838-187">-Tags</span></span>
<span data-ttu-id="b8838-188">Określa słownik par klucz-wartość w postaci tabeli skrótu, który to polecenie cmdlet skojarzy z nową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="b8838-188">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="b8838-189">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="b8838-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b8838-190">— VCore</span><span class="sxs-lookup"><span data-stu-id="b8838-190">-VCore</span></span>
<span data-ttu-id="b8838-191">Numer Vcore bazy danych Azure Sql Database</span><span class="sxs-lookup"><span data-stu-id="b8838-191">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="b8838-192">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="b8838-192">-ZoneRedundant</span></span>
<span data-ttu-id="b8838-193">Nadmiarowość stref do skojarzenia z usługą Azure Sql Database</span><span class="sxs-lookup"><span data-stu-id="b8838-193">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="b8838-194">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8838-194">-Confirm</span></span>
<span data-ttu-id="b8838-195">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8838-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8838-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8838-196">-WhatIf</span></span>
<span data-ttu-id="b8838-197">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8838-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8838-198">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b8838-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8838-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8838-199">CommonParameters</span></span>
<span data-ttu-id="b8838-200">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8838-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8838-201">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8838-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8838-202">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8838-202">INPUTS</span></span>

### <span data-ttu-id="b8838-203">System.String</span><span class="sxs-lookup"><span data-stu-id="b8838-203">System.String</span></span>

## <span data-ttu-id="b8838-204">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8838-204">OUTPUTS</span></span>

### <span data-ttu-id="b8838-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b8838-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b8838-206">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8838-206">NOTES</span></span>

## <span data-ttu-id="b8838-207">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8838-207">RELATED LINKS</span></span>

[<span data-ttu-id="b8838-208">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8838-208">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="b8838-209">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b8838-209">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="b8838-210">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="b8838-210">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="b8838-211">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8838-211">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="b8838-212">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8838-212">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="b8838-213">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8838-213">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="b8838-214">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8838-214">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="b8838-215">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b8838-215">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

