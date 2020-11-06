---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: b4c444233701a6ecfe66eb77f90dade618c9e08f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546400"
---
# <span data-ttu-id="894ea-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="894ea-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="894ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="894ea-102">SYNOPSIS</span></span>
<span data-ttu-id="894ea-103">Przywraca bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="894ea-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="894ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="894ea-104">SYNTAX</span></span>

### <span data-ttu-id="894ea-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="894ea-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="894ea-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="894ea-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="894ea-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="894ea-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="894ea-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="894ea-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="894ea-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="894ea-109">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="894ea-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="894ea-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="894ea-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="894ea-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="894ea-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="894ea-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="894ea-113">Opis</span><span class="sxs-lookup"><span data-stu-id="894ea-113">DESCRIPTION</span></span>
<span data-ttu-id="894ea-114">Polecenie cmdlet **Restore-AzureRmSqlDatabase** przywraca bazę danych SQL z kopii zapasowej Geo-rezerwowej, kopii zapasowej usuniętej bazy danych, kopii zapasowej długotrwałego przechowywania lub punktu w czasie w bazie danych na żywo.</span><span class="sxs-lookup"><span data-stu-id="894ea-114">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="894ea-115">Przywrócona baza danych zostanie utworzona jako nowa baza danych.</span><span class="sxs-lookup"><span data-stu-id="894ea-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="894ea-116">Można utworzyć elastyczną bazę danych SQL, ustawiając parametr *ElasticPoolName* na istniejącą pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="894ea-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="894ea-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="894ea-117">EXAMPLES</span></span>

### <span data-ttu-id="894ea-118">Przykład 1: Przywracanie bazy danych z punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="894ea-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="894ea-119">Pierwsze polecenie pobiera bazę danych SQL o nazwie Database01, a następnie zapisuje ją w zmiennej $Database.</span><span class="sxs-lookup"><span data-stu-id="894ea-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="894ea-120">Drugie polecenie przywraca bazę danych w $Database z określonego momentu kopii zapasowej do bazy danych o nazwie RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="894ea-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="894ea-121">Przykład 2: Przywracanie bazy danych od punktu w czasie do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="894ea-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="894ea-122">Pierwsze polecenie pobiera bazę danych SQL o nazwie Database01, a następnie zapisuje ją w zmiennej $Database.</span><span class="sxs-lookup"><span data-stu-id="894ea-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="894ea-123">Drugie polecenie przywraca bazę danych w $Database z określonego momentu kopii zapasowej bazy danych SQL o nazwie RestoredDatabase w elastycznej puli o nazwie elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="894ea-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="894ea-124">Przykład 3: Przywracanie usuniętej bazy danych</span><span class="sxs-lookup"><span data-stu-id="894ea-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="894ea-125">Pierwsze polecenie powoduje pobranie usuniętej kopii zapasowej bazy danych, która ma zostać przywrócona przy użyciu polecenia [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="894ea-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="894ea-126">Drugie polecenie rozpoczyna przywracanie z usuniętej kopii zapasowej bazy danych przy użyciu polecenia cmdlet [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="894ea-126">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="894ea-127">Jeśli nie określono parametru-PointInTime, baza danych zostanie przywrócona do godziny usunięcia.</span><span class="sxs-lookup"><span data-stu-id="894ea-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="894ea-128">Przykład 4: Przywracanie usuniętej bazy danych do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="894ea-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="894ea-129">Pierwsze polecenie powoduje pobranie usuniętej kopii zapasowej bazy danych, która ma zostać przywrócona przy użyciu polecenia [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="894ea-129">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="894ea-130">Drugie polecenie rozpoczyna przywracanie z usuniętej kopii zapasowej bazy danych za pomocą polecenia [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="894ea-130">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="894ea-131">Jeśli nie określono parametru-PointInTime, baza danych zostanie przywrócona do godziny usunięcia.</span><span class="sxs-lookup"><span data-stu-id="894ea-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="894ea-132">Przykład 5: Geo-Restore bazy danych</span><span class="sxs-lookup"><span data-stu-id="894ea-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="894ea-133">Pierwsze polecenie pobiera kopię zapasową Geo-nadmiarową bazy danych o nazwie Database01, a następnie zapisuje ją w zmiennej $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="894ea-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="894ea-134">Drugie polecenie przywraca kopię zapasową w $GeoBackup bazie danych SQL o nazwie RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="894ea-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="894ea-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="894ea-135">PARAMETERS</span></span>

### <span data-ttu-id="894ea-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="894ea-136">-AsJob</span></span>
<span data-ttu-id="894ea-137">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="894ea-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="894ea-138">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="894ea-138">-ComputeGeneration</span></span>
<span data-ttu-id="894ea-139">Generowanie obliczeń do przypisania do przywróconej bazy danych</span><span class="sxs-lookup"><span data-stu-id="894ea-139">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="894ea-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894ea-140">-DefaultProfile</span></span>
<span data-ttu-id="894ea-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="894ea-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="894ea-142">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="894ea-142">-DeletionDate</span></span>
<span data-ttu-id="894ea-143">Określa datę usunięcia jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="894ea-143">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="894ea-144">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="894ea-144">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="894ea-145">-Edition</span><span class="sxs-lookup"><span data-stu-id="894ea-145">-Edition</span></span>
<span data-ttu-id="894ea-146">Określa wersję bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="894ea-146">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="894ea-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="894ea-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="894ea-148">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="894ea-148">None</span></span>
- <span data-ttu-id="894ea-149">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="894ea-149">Basic</span></span>
- <span data-ttu-id="894ea-150">Standard</span><span class="sxs-lookup"><span data-stu-id="894ea-150">Standard</span></span>
- <span data-ttu-id="894ea-151">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="894ea-151">Premium</span></span>
- <span data-ttu-id="894ea-152">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="894ea-152">DataWarehouse</span></span>
- <span data-ttu-id="894ea-153">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="894ea-153">Free</span></span>
- <span data-ttu-id="894ea-154">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="894ea-154">Stretch</span></span>
- <span data-ttu-id="894ea-155">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="894ea-155">GeneralPurpose</span></span>
- <span data-ttu-id="894ea-156">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="894ea-156">BusinessCritical</span></span>

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

### <span data-ttu-id="894ea-157">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="894ea-157">-ElasticPoolName</span></span>
<span data-ttu-id="894ea-158">Określa nazwę puli elastycznej, w której ma zostać umieszczona baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="894ea-158">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="894ea-159">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="894ea-159">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="894ea-160">Wskazuje, że to polecenie cmdlet przywraca bazę danych z kopii zapasowej usuniętej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="894ea-160">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="894ea-161">Możesz użyć polecenia cmdlet Get-AzureRMSqlDeletedDatabaseBackup, aby pobrać kopię zapasową usuniętej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="894ea-161">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="894ea-162">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="894ea-162">-FromGeoBackup</span></span>
<span data-ttu-id="894ea-163">Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL z kopii zapasowej Geo-nadmiarowej.</span><span class="sxs-lookup"><span data-stu-id="894ea-163">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="894ea-164">Możesz użyć polecenia cmdlet Get-AzureRMSqlDatabaseGeoBackup, aby uzyskać kopię zapasową Geo-nadmiarową.</span><span class="sxs-lookup"><span data-stu-id="894ea-164">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="894ea-165">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="894ea-165">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="894ea-166">Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL po długim czasie przechowywania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="894ea-166">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="894ea-167">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="894ea-167">-FromPointInTimeBackup</span></span>
<span data-ttu-id="894ea-168">Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL z kopii zapasowej w czasie.</span><span class="sxs-lookup"><span data-stu-id="894ea-168">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="894ea-169">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="894ea-169">-LicenseType</span></span>
<span data-ttu-id="894ea-170">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="894ea-170">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="894ea-171">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="894ea-171">-PointInTime</span></span>
<span data-ttu-id="894ea-172">Określa punkt w postaci obiektu **DateTime** , na który ma być przywracana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="894ea-172">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="894ea-173">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="894ea-173">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="894ea-174">Ten parametr jest używany razem z parametrem *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="894ea-174">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="894ea-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="894ea-175">-ResourceGroupName</span></span>
<span data-ttu-id="894ea-176">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisuje bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="894ea-176">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="894ea-177">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="894ea-177">-ResourceId</span></span>
<span data-ttu-id="894ea-178">Określa identyfikator zasobu do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="894ea-178">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="894ea-179">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="894ea-179">-ServerName</span></span>
<span data-ttu-id="894ea-180">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="894ea-180">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="894ea-181">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="894ea-181">-ServiceObjectiveName</span></span>
<span data-ttu-id="894ea-182">Określa nazwę celu usługi.</span><span class="sxs-lookup"><span data-stu-id="894ea-182">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="894ea-183">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="894ea-183">-TargetDatabaseName</span></span>
<span data-ttu-id="894ea-184">Określa nazwę bazy danych, do której ma zostać przywrócona operacja.</span><span class="sxs-lookup"><span data-stu-id="894ea-184">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="894ea-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="894ea-185">-VCore</span></span>
<span data-ttu-id="894ea-186">Numery vCore przywróconej bazy danych platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="894ea-186">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="894ea-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894ea-187">CommonParameters</span></span>
<span data-ttu-id="894ea-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894ea-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894ea-189">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="894ea-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894ea-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="894ea-190">INPUTS</span></span>

### <span data-ttu-id="894ea-191">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="894ea-191">System.DateTime</span></span>

### <span data-ttu-id="894ea-192">System. String</span><span class="sxs-lookup"><span data-stu-id="894ea-192">System.String</span></span>

## <span data-ttu-id="894ea-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="894ea-193">OUTPUTS</span></span>

### <span data-ttu-id="894ea-194">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="894ea-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="894ea-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="894ea-195">NOTES</span></span>

## <span data-ttu-id="894ea-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="894ea-196">RELATED LINKS</span></span>

[<span data-ttu-id="894ea-197">Odzyskiwanie bazy danych SQL Azure z awarii</span><span class="sxs-lookup"><span data-stu-id="894ea-197">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="894ea-198">Odzyskiwanie bazy danych SQL Azure przy użyciu błędu użytkownika</span><span class="sxs-lookup"><span data-stu-id="894ea-198">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="894ea-199">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="894ea-199">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="894ea-200">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="894ea-200">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="894ea-201">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="894ea-201">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="894ea-202">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="894ea-202">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

