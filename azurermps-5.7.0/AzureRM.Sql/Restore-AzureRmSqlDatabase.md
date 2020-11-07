---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: e7110511840542b8efed22b1267b76074434b94a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716813"
---
# <span data-ttu-id="5060e-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5060e-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="5060e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5060e-102">SYNOPSIS</span></span>
<span data-ttu-id="5060e-103">Przywraca bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5060e-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5060e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5060e-104">SYNTAX</span></span>

### <span data-ttu-id="5060e-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="5060e-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5060e-106">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="5060e-106">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5060e-107">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="5060e-107">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5060e-108">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="5060e-108">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5060e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5060e-109">DESCRIPTION</span></span>
<span data-ttu-id="5060e-110">Polecenie cmdlet **Restore-AzureRmSqlDatabase** przywraca bazę danych SQL z kopii zapasowej Geo-rezerwowej, kopii zapasowej usuniętej bazy danych, kopii zapasowej długotrwałego przechowywania lub punktu w czasie w bazie danych na żywo.</span><span class="sxs-lookup"><span data-stu-id="5060e-110">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="5060e-111">Przywrócona baza danych zostanie utworzona jako nowa baza danych.</span><span class="sxs-lookup"><span data-stu-id="5060e-111">The restored database is created as a new database.</span></span>

<span data-ttu-id="5060e-112">Można utworzyć elastyczną bazę danych SQL, ustawiając parametr *ElasticPoolName* na istniejącą pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="5060e-112">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="5060e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5060e-113">EXAMPLES</span></span>

### <span data-ttu-id="5060e-114">Przykład 1: Przywracanie bazy danych z punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="5060e-114">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="5060e-115">Pierwsze polecenie pobiera bazę danych SQL o nazwie Database01, a następnie zapisuje ją w zmiennej $Database.</span><span class="sxs-lookup"><span data-stu-id="5060e-115">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="5060e-116">Drugie polecenie przywraca bazę danych w $Database z określonego momentu kopii zapasowej do bazy danych o nazwie RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="5060e-116">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="5060e-117">Przykład 2: Przywracanie bazy danych od punktu w czasie do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="5060e-117">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="5060e-118">Pierwsze polecenie pobiera bazę danych SQL o nazwie Database01, a następnie zapisuje ją w zmiennej $Database.</span><span class="sxs-lookup"><span data-stu-id="5060e-118">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="5060e-119">Drugie polecenie przywraca bazę danych w $Database z określonego momentu kopii zapasowej bazy danych SQL o nazwie RestoredDatabase w elastycznej puli o nazwie elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="5060e-119">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="5060e-120">Przykład 3: Przywracanie usuniętej bazy danych</span><span class="sxs-lookup"><span data-stu-id="5060e-120">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="5060e-121">Pierwsze polecenie powoduje pobranie usuniętej kopii zapasowej bazy danych, która ma zostać przywrócona przy użyciu polecenia [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="5060e-121">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="5060e-122">Drugie polecenie rozpoczyna przywracanie z usuniętej kopii zapasowej bazy danych przy użyciu polecenia cmdlet [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="5060e-122">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="5060e-123">Jeśli nie określono parametru-PointInTime, baza danych zostanie przywrócona do godziny usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5060e-123">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="5060e-124">Przykład 4: Przywracanie usuniętej bazy danych do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="5060e-124">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="5060e-125">Pierwsze polecenie powoduje pobranie usuniętej kopii zapasowej bazy danych, która ma zostać przywrócona przy użyciu polecenia [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="5060e-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="5060e-126">Drugie polecenie rozpoczyna przywracanie z usuniętej kopii zapasowej bazy danych za pomocą polecenia [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="5060e-126">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="5060e-127">Jeśli nie określono parametru-PointInTime, baza danych zostanie przywrócona do godziny usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5060e-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="5060e-128">Przykład 5: Geo-Restore bazy danych</span><span class="sxs-lookup"><span data-stu-id="5060e-128">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="5060e-129">Pierwsze polecenie pobiera kopię zapasową Geo-nadmiarową bazy danych o nazwie Database01, a następnie zapisuje ją w zmiennej $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="5060e-129">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>

<span data-ttu-id="5060e-130">Drugie polecenie przywraca kopię zapasową w $GeoBackup bazie danych SQL o nazwie RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="5060e-130">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="5060e-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5060e-131">PARAMETERS</span></span>

### <span data-ttu-id="5060e-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5060e-132">-AsJob</span></span>
<span data-ttu-id="5060e-133">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5060e-133">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5060e-134">-DefaultProfile</span></span>
<span data-ttu-id="5060e-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5060e-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-136">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="5060e-136">-DeletionDate</span></span>
<span data-ttu-id="5060e-137">Określa datę usunięcia jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="5060e-137">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="5060e-138">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="5060e-138">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="5060e-139">-Edition</span></span>
<span data-ttu-id="5060e-140">Określa wersję bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5060e-140">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="5060e-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5060e-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5060e-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5060e-142">None</span></span>
- <span data-ttu-id="5060e-143">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="5060e-143">Premium</span></span>
- <span data-ttu-id="5060e-144">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="5060e-144">Basic</span></span>
- <span data-ttu-id="5060e-145">Standard</span><span class="sxs-lookup"><span data-stu-id="5060e-145">Standard</span></span>
- <span data-ttu-id="5060e-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="5060e-146">DataWarehouse</span></span>
- <span data-ttu-id="5060e-147">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="5060e-147">Free</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-148">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5060e-148">-ElasticPoolName</span></span>
<span data-ttu-id="5060e-149">Określa nazwę puli elastycznej, w której ma zostać umieszczona baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5060e-149">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-150">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="5060e-150">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="5060e-151">Wskazuje, że to polecenie cmdlet przywraca bazę danych z kopii zapasowej usuniętej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5060e-151">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="5060e-152">Możesz użyć polecenia cmdlet Get-AzureRMSqlDeletedDatabaseBackup, aby pobrać kopię zapasową usuniętej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5060e-152">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-153">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="5060e-153">-FromGeoBackup</span></span>
<span data-ttu-id="5060e-154">Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL z kopii zapasowej Geo-nadmiarowej.</span><span class="sxs-lookup"><span data-stu-id="5060e-154">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="5060e-155">Możesz użyć polecenia cmdlet Get-AzureRMSqlDatabaseGeoBackup, aby uzyskać kopię zapasową Geo-nadmiarową.</span><span class="sxs-lookup"><span data-stu-id="5060e-155">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromGeoBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-156">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="5060e-156">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="5060e-157">Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL po długim czasie przechowywania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="5060e-157">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-158">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="5060e-158">-FromPointInTimeBackup</span></span>
<span data-ttu-id="5060e-159">Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL z kopii zapasowej w czasie.</span><span class="sxs-lookup"><span data-stu-id="5060e-159">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-160">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="5060e-160">-PointInTime</span></span>
<span data-ttu-id="5060e-161">Określa punkt w postaci obiektu **DateTime** , na który ma być przywracana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5060e-161">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="5060e-162">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="5060e-162">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>

<span data-ttu-id="5060e-163">Ten parametr jest używany razem z parametrem *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="5060e-163">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: DateTime
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5060e-164">-ResourceGroupName</span></span>
<span data-ttu-id="5060e-165">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisuje bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5060e-165">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5060e-166">-ResourceId</span></span>
<span data-ttu-id="5060e-167">Określa identyfikator zasobu do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="5060e-167">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-168">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5060e-168">-ServerName</span></span>
<span data-ttu-id="5060e-169">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5060e-169">Specifies the name of the SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-170">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="5060e-170">-ServiceObjectiveName</span></span>
<span data-ttu-id="5060e-171">Określa nazwę celu usługi.</span><span class="sxs-lookup"><span data-stu-id="5060e-171">Specifies the name of the service objective.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-172">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5060e-172">-TargetDatabaseName</span></span>
<span data-ttu-id="5060e-173">Określa nazwę bazy danych, do której ma zostać przywrócona operacja.</span><span class="sxs-lookup"><span data-stu-id="5060e-173">Specifies the name of the database to restore to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5060e-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5060e-174">CommonParameters</span></span>
<span data-ttu-id="5060e-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5060e-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5060e-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5060e-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5060e-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5060e-177">INPUTS</span></span>

### <span data-ttu-id="5060e-178">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5060e-178">None</span></span>
<span data-ttu-id="5060e-179">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5060e-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5060e-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5060e-180">OUTPUTS</span></span>

### <span data-ttu-id="5060e-181">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5060e-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5060e-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5060e-182">NOTES</span></span>

## <span data-ttu-id="5060e-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5060e-183">RELATED LINKS</span></span>

[<span data-ttu-id="5060e-184">Odzyskiwanie bazy danych SQL Azure z awarii</span><span class="sxs-lookup"><span data-stu-id="5060e-184">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="5060e-185">Odzyskiwanie bazy danych SQL Azure przy użyciu błędu użytkownika</span><span class="sxs-lookup"><span data-stu-id="5060e-185">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="5060e-186">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5060e-186">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="5060e-187">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="5060e-187">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="5060e-188">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="5060e-188">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="5060e-189">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5060e-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

