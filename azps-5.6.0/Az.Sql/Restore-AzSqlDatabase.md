---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: bfe2abe8a59114f69ec27f28ba0b270bfbbd72a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995051"
---
# <span data-ttu-id="91160-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91160-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="91160-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91160-102">SYNOPSIS</span></span>
<span data-ttu-id="91160-103">Przywraca bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="91160-103">Restores a SQL database.</span></span>

## <span data-ttu-id="91160-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91160-104">SYNTAX</span></span>

### <span data-ttu-id="91160-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="91160-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91160-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="91160-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91160-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="91160-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91160-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="91160-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91160-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="91160-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91160-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="91160-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91160-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="91160-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91160-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="91160-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91160-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="91160-113">DESCRIPTION</span></span>
<span data-ttu-id="91160-114">Polecenie cmdlet **Restore-AzSqlDatabase** przywraca bazę danych SQL z nadmiarowej geograficznej kopii zapasowej, kopii zapasowej usuniętej bazy danych, długookresowej kopii zapasowej przechowywania lub punktu w czasie w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="91160-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="91160-115">Przywrócona baza danych zostanie utworzona jako nowa baza danych.</span><span class="sxs-lookup"><span data-stu-id="91160-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="91160-116">Możesz utworzyć elastyczną bazę danych SQL, ustawiając dla *parametru AAA parametr 10001* istniejącą pulę elastycznego buforu.</span><span class="sxs-lookup"><span data-stu-id="91160-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="91160-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91160-117">EXAMPLES</span></span>

### <span data-ttu-id="91160-118">Przykład 1. Przywracanie bazy danych z punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="91160-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="91160-119">Pierwsze polecenie pobiera bazę danych SQL o nazwie Database01, a następnie zapisuje ją w $Database zmienną.</span><span class="sxs-lookup"><span data-stu-id="91160-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="91160-120">Drugie polecenie przywraca bazę danych w $Database kopii zapasowej z określonego punktu w czasie do bazy danych o nazwie RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="91160-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="91160-121">Przykład 2. Przywracanie bazy danych z miejsca do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="91160-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="91160-122">Pierwsze polecenie pobiera bazę danych SQL o nazwie Database01, a następnie zapisuje ją w $Database zmienną.</span><span class="sxs-lookup"><span data-stu-id="91160-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="91160-123">Drugie polecenie przywraca bazę danych w programie $Database z określonej kopii zapasowej z określonego punktu w czasie do bazy danych SQL o nazwie RestoredDatabase w puli elastycznej o nazwiePool01.</span><span class="sxs-lookup"><span data-stu-id="91160-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="91160-124">Przykład 3. Przywracanie usuniętej bazy danych</span><span class="sxs-lookup"><span data-stu-id="91160-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="91160-125">Pierwsze polecenie pobiera usuniętą kopię zapasową bazy danych, którą chcesz przywrócić przy użyciu polecenia [Get-AzSqlDeletedDatabaseBackup.](./Get-AzSqlDeletedDatabaseBackup.md)</span><span class="sxs-lookup"><span data-stu-id="91160-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="91160-126">Drugie polecenie uruchamia przywracanie z usuniętej kopii zapasowej bazy danych za pomocą polecenia cmdlet [Restore-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="91160-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="91160-127">Jeśli parametr -PointInTime nie zostanie określony, baza danych zostanie przywrócona do czasu usunięcia.</span><span class="sxs-lookup"><span data-stu-id="91160-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="91160-128">Przykład 4. Przywracanie usuniętej bazy danych do elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="91160-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="91160-129">Pierwsze polecenie pobiera usuniętą kopię zapasową bazy danych, którą chcesz przywrócić przy użyciu polecenia [Get-AzSqlDeletedDatabaseBackup.](./Get-AzSqlDeletedDatabaseBackup.md)</span><span class="sxs-lookup"><span data-stu-id="91160-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="91160-130">Drugie polecenie uruchamia przywracanie z usuniętej kopii zapasowej bazy danych przy użyciu [polecenia Przywróć-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="91160-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="91160-131">Jeśli parametr -PointInTime nie zostanie określony, baza danych zostanie przywrócona do czasu usunięcia.</span><span class="sxs-lookup"><span data-stu-id="91160-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="91160-132">Przykład 5. Geo-Restore bazy danych</span><span class="sxs-lookup"><span data-stu-id="91160-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="91160-133">Pierwsze polecenie pobiera nadmiarową geograficznie kopię zapasową bazy danych o nazwie Database01, a następnie przechowuje ją w $GeoBackup danych.</span><span class="sxs-lookup"><span data-stu-id="91160-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="91160-134">Drugie polecenie przywraca kopię zapasową w $GeoBackup do bazy danych SQL o nazwie RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="91160-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="91160-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91160-135">PARAMETERS</span></span>

### <span data-ttu-id="91160-136">— AsJob</span><span class="sxs-lookup"><span data-stu-id="91160-136">-AsJob</span></span>
<span data-ttu-id="91160-137">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="91160-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91160-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="91160-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="91160-139">Nadmiarowość magazynu kopii zapasowej używana do przechowywania kopii zapasowych dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="91160-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="91160-140">Dostępne są następujące opcje: Lokalny, Strefa i Geo.</span><span class="sxs-lookup"><span data-stu-id="91160-140">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="91160-141">-Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="91160-141">-ComputeGeneration</span></span>
<span data-ttu-id="91160-142">Generowanie obliczeń do przypisania do przywróconej bazy danych</span><span class="sxs-lookup"><span data-stu-id="91160-142">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91160-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91160-143">-DefaultProfile</span></span>
<span data-ttu-id="91160-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="91160-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91160-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="91160-145">-DeletionDate</span></span>
<span data-ttu-id="91160-146">Określa datę usunięcia jako obiekt **DateTime.**</span><span class="sxs-lookup"><span data-stu-id="91160-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="91160-147">Aby uzyskać obiekt **DateTime,** użyj Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91160-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91160-148">— wersja</span><span class="sxs-lookup"><span data-stu-id="91160-148">-Edition</span></span>
<span data-ttu-id="91160-149">Określa wersję bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="91160-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="91160-150">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="91160-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91160-151">Brak</span><span class="sxs-lookup"><span data-stu-id="91160-151">None</span></span>
- <span data-ttu-id="91160-152">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="91160-152">Basic</span></span>
- <span data-ttu-id="91160-153">Standardowe</span><span class="sxs-lookup"><span data-stu-id="91160-153">Standard</span></span>
- <span data-ttu-id="91160-154">Premium</span><span class="sxs-lookup"><span data-stu-id="91160-154">Premium</span></span>
- <span data-ttu-id="91160-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="91160-155">DataWarehouse</span></span>
- <span data-ttu-id="91160-156">Bezpłatne</span><span class="sxs-lookup"><span data-stu-id="91160-156">Free</span></span>
- <span data-ttu-id="91160-157">Rozciągnięcie</span><span class="sxs-lookup"><span data-stu-id="91160-157">Stretch</span></span>
- <span data-ttu-id="91160-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="91160-158">GeneralPurpose</span></span>
- <span data-ttu-id="91160-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="91160-159">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91160-160">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="91160-160">-ElasticPoolName</span></span>
<span data-ttu-id="91160-161">Określa nazwę puli elastycznej, w której ma być umieszczana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="91160-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91160-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="91160-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="91160-163">Wskazuje, że to polecenie cmdlet przywraca bazę danych z usuniętej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="91160-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="91160-164">Za pomocą tego Get-AzSqlDeletedDatabaseBackup cmdlet można uzyskać kopię zapasową usuniętej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="91160-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91160-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="91160-165">-FromGeoBackup</span></span>
<span data-ttu-id="91160-166">Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL z nadmiarowej geograficznej kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="91160-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="91160-167">Możesz użyć tego Get-AzSqlDatabaseGeoBackup cmdlet, aby uzyskać geograficznie nadmiarową kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="91160-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91160-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="91160-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="91160-169">Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL z długookresowej kopii zapasowej przechowywania.</span><span class="sxs-lookup"><span data-stu-id="91160-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91160-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="91160-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="91160-171">Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL z kopii zapasowej w momencie.</span><span class="sxs-lookup"><span data-stu-id="91160-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91160-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="91160-172">-LicenseType</span></span>
<span data-ttu-id="91160-173">Typ licencji dla bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="91160-173">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="91160-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="91160-174">-PointInTime</span></span>
<span data-ttu-id="91160-175">Określa punkt w czasie jako obiekt **DateTime,** do którego chcesz przywrócić bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="91160-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="91160-176">Aby uzyskać obiekt **DateTime,** użyj polecenia cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="91160-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="91160-177">Użyj tego parametru razem z *parametrem FromPointInTimeBackup.*</span><span class="sxs-lookup"><span data-stu-id="91160-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91160-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91160-178">-ResourceGroupName</span></span>
<span data-ttu-id="91160-179">Określa nazwę grupy zasobów, do której to polecenie cmdlet przypisuje bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="91160-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="91160-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91160-180">-ResourceId</span></span>
<span data-ttu-id="91160-181">Określa identyfikator zasobu do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="91160-181">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91160-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="91160-182">-ServerName</span></span>
<span data-ttu-id="91160-183">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="91160-183">Specifies the name of the SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91160-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="91160-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="91160-185">Określa nazwę celu usługi.</span><span class="sxs-lookup"><span data-stu-id="91160-185">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91160-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="91160-186">-TargetDatabaseName</span></span>
<span data-ttu-id="91160-187">Określa nazwę bazy danych, do która ma zostać przywrócona.</span><span class="sxs-lookup"><span data-stu-id="91160-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="91160-188">— VCore</span><span class="sxs-lookup"><span data-stu-id="91160-188">-VCore</span></span>
<span data-ttu-id="91160-189">Numery vcore przywróconej bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="91160-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91160-190">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91160-190">-Confirm</span></span>
<span data-ttu-id="91160-191">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="91160-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91160-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91160-192">-WhatIf</span></span>
<span data-ttu-id="91160-193">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91160-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91160-194">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="91160-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91160-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91160-195">CommonParameters</span></span>
<span data-ttu-id="91160-196">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91160-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91160-197">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91160-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91160-198">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91160-198">INPUTS</span></span>

### <span data-ttu-id="91160-199">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="91160-199">System.DateTime</span></span>

### <span data-ttu-id="91160-200">System.String</span><span class="sxs-lookup"><span data-stu-id="91160-200">System.String</span></span>

## <span data-ttu-id="91160-201">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91160-201">OUTPUTS</span></span>

### <span data-ttu-id="91160-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="91160-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="91160-203">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91160-203">NOTES</span></span>

## <span data-ttu-id="91160-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91160-204">RELATED LINKS</span></span>

[<span data-ttu-id="91160-205">Odzyskiwanie bazy danych Azure SQL Database po 30-55 dniach</span><span class="sxs-lookup"><span data-stu-id="91160-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="91160-206">Odzyskiwanie bazy danych Azure SQL Database po błędzie użytkownika</span><span class="sxs-lookup"><span data-stu-id="91160-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="91160-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91160-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="91160-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="91160-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="91160-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="91160-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="91160-210">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="91160-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

