---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: 9b87539335752b07b6c03852f30959b13de4c06e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201411"
---
# <span data-ttu-id="ca66c-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ca66c-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="ca66c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca66c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca66c-103">Przywraca bazę danych azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="ca66c-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="ca66c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca66c-104">SYNTAX</span></span>

### <span data-ttu-id="ca66c-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ca66c-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca66c-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ca66c-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca66c-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ca66c-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca66c-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="ca66c-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca66c-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ca66c-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca66c-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ca66c-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca66c-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="ca66c-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca66c-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="ca66c-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca66c-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameters</span><span class="sxs-lookup"><span data-stu-id="ca66c-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca66c-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="ca66c-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca66c-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameters</span><span class="sxs-lookup"><span data-stu-id="ca66c-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-Name] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca66c-116">LongTermRetentionBackupRestoreParameters</span><span class="sxs-lookup"><span data-stu-id="ca66c-116">LongTermRetentionBackupRestoreParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromLongTermRetentionBackup] [-SubscriptionId <String>] [-ResourceId] <String>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca66c-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca66c-117">DESCRIPTION</span></span>
<span data-ttu-id="ca66c-118">Polecenie cmdlet **Restore-AzSqlInstanceDatabase** przywraca bazę danych wystąpienia z nadmiarowej geograficznej kopii zapasowej, punktu w czasie w bazie danych lub z długookresowej kopii zapasowej przechowywania.</span><span class="sxs-lookup"><span data-stu-id="ca66c-118">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup, a point in time in a live database, or a long term retention backup.</span></span>
<span data-ttu-id="ca66c-119">Przywrócona baza danych zostanie utworzona jako baza danych nowego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ca66c-119">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="ca66c-120">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca66c-120">EXAMPLES</span></span>

### <span data-ttu-id="ca66c-121">Przykład 1. Przywracanie bazy danych wystąpienia z punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="ca66c-121">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="ca66c-122">To polecenie przywraca wystąpienie bazy danych Database01 z określonej kopii zapasowej z określonego punktu w czasie do bazy danych wystąpienia o nazwie Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="ca66c-122">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="ca66c-123">Przykład 2. Przywracanie bazy danych wystąpienia z punktu w czasie do innego wystąpienia w innej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ca66c-123">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="ca66c-124">To polecenie przywraca wystąpienie bazy danych Database01 w wystąpieniu danych managedInstance1 w grupie zasobów ResourceGroup01 z określonej kopii zapasowej z określonego punktu w czasie do bazy danych wystąpienia o nazwie Database01_restored w wystąpieniu managedInstance2 w grupie zasobów ResourceGroup02.</span><span class="sxs-lookup"><span data-stu-id="ca66c-124">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="ca66c-125">Przykład 3. Geo-Restore bazy danych wystąpienia</span><span class="sxs-lookup"><span data-stu-id="ca66c-125">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="ca66c-126">Pierwsze polecenie pobiera nadmiarową geograficznie kopię zapasową bazy danych o nazwie Database01, a następnie przechowuje ją w $GeoBackup danych.</span><span class="sxs-lookup"><span data-stu-id="ca66c-126">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="ca66c-127">Drugie polecenie przywraca kopię zapasową w $GeoBackup do bazy danych wystąpienia o nazwie Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="ca66c-127">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="ca66c-128">Przykład 4. Przywracanie bazy danych usuniętego wystąpienia z punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="ca66c-128">Example 4: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -FromPointInTimeBackup -Name $deletedDatabase.Name -InstanceName $deletedDatabase.ManagedInstanceName -ResourceGroupName $deletedDatabase.ResourceGroupName -DeletionDate $deletedDatabase.DeletionDate -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="ca66c-129">Pierwsze polecenie pobiera bazy danych usuniętego wystąpienia o nazwie "DB1" w wystąpieniu "managedInstance1".</span><span class="sxs-lookup"><span data-stu-id="ca66c-129">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="ca66c-130">Drugie polecenie przywraca dostępną bazę danych z kopii zapasowej określonej kopii zapasowej z określonego punktu w czasie do bazy danych wystąpienia o nazwie Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="ca66c-130">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="ca66c-131">Przykład 5. Przywracanie bazy danych usuniętego wystąpienia z punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="ca66c-131">Example 5: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -FromPointInTimeBackup -InputObject $deletedDatabase[0] -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="ca66c-132">Pierwsze polecenie pobiera bazy danych usuniętego wystąpienia o nazwie "DB1" w wystąpieniu "managedInstance1".</span><span class="sxs-lookup"><span data-stu-id="ca66c-132">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="ca66c-133">Drugie polecenie przywraca dostępną bazę danych z określonej kopii zapasowej w momencie do wystąpienia bazy danych o nazwie Database01_restored przy użyciu obiektu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="ca66c-133">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored using input object.</span></span>

### <span data-ttu-id="ca66c-134">Przykład 6. Przywracanie bazy danych z kopii zapasowej LTR.</span><span class="sxs-lookup"><span data-stu-id="ca66c-134">Example 6: Restore a database from LTR backup.</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -FromLongTermRetentionBackup -ResourceId /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManagedInstances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000 -TargetInstanceDatabaseName restoreTarget -TargetInstanceName testInstance -TargetResourceGroupName testResourceGroup


Location                          : southeastasia
Tags                              :
Collation                         : SQL_Latin1_General_CP1_CI_AS
Status                            : Online
RestorePointInTime                :
DefaultSecondaryLocation          : northeurope
CatalogCollation                  :
CreateMode                        :
StorageContainerUri               :
StorageContainerSasToken          :
SourceDatabaseId                  :
FailoverGroupId                   :
RecoverableDatabaseId             :
RestorableDroppedDatabaseId       :
LongTermRetentionBackupResourceId :
ResourceGroupName                 : testResourceGroup
ManagedInstanceName               : testInstance
Name                              : restoreTarget
CreationDate                      : 3/4/2020 8:12:56 AM
EarliestRestorePoint              : 3/4/2020 8:14:29 AM
Id                                : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/managedInstances/testInstance/databases/restoreTarget
```

<span data-ttu-id="ca66c-135">Przywraca kopię zapasową LTR z danym identyfikatorem zasobu (który można znaleźć, uruchamiając program Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span><span class="sxs-lookup"><span data-stu-id="ca66c-135">Restores LTR backup with the given resource ID (which can be found by running Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span></span>

## <span data-ttu-id="ca66c-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca66c-136">PARAMETERS</span></span>

### <span data-ttu-id="ca66c-137">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ca66c-137">-AsJob</span></span>
<span data-ttu-id="ca66c-138">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ca66c-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca66c-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca66c-139">-DefaultProfile</span></span>
<span data-ttu-id="ca66c-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ca66c-140">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="ca66c-141">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="ca66c-141">-DeletionDate</span></span>
<span data-ttu-id="ca66c-142">Data usunięcia usuniętej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ca66c-142">The deletion date of deleted database.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-143">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ca66c-143">-FromGeoBackup</span></span>
<span data-ttu-id="ca66c-144">Przywracanie z kopii zapasowej geolokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ca66c-144">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-145">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ca66c-145">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="ca66c-146">Przywracanie z kopii zapasowej przechowywania długoterminowego.</span><span class="sxs-lookup"><span data-stu-id="ca66c-146">Restore from a Long Term Retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-147">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="ca66c-147">-FromPointInTimeBackup</span></span>
<span data-ttu-id="ca66c-148">Przywracanie z kopii zapasowej z punktu w czasie.</span><span class="sxs-lookup"><span data-stu-id="ca66c-148">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-149">- GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="ca66c-149">-GeoBackupObject</span></span>
<span data-ttu-id="ca66c-150">Obiekt bazy danych wystąpienia, który można przywrócić</span><span class="sxs-lookup"><span data-stu-id="ca66c-150">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-151">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca66c-151">-InputObject</span></span>
<span data-ttu-id="ca66c-152">Obiekt Instance Database do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="ca66c-152">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-153">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ca66c-153">-InstanceName</span></span>
<span data-ttu-id="ca66c-154">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ca66c-154">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-155">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ca66c-155">-Name</span></span>
<span data-ttu-id="ca66c-156">Nazwa bazy danych wystąpienia, która ma zostać przywrócona.</span><span class="sxs-lookup"><span data-stu-id="ca66c-156">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName, SourceInstanceDatabaseName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-157">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="ca66c-157">-PointInTime</span></span>
<span data-ttu-id="ca66c-158">Czas na przywrócenie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ca66c-158">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca66c-159">-ResourceGroupName</span></span>
<span data-ttu-id="ca66c-160">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca66c-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca66c-161">-ResourceId</span></span>
<span data-ttu-id="ca66c-162">Identyfikator zasobu obiektu instance database do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="ca66c-162">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-163">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca66c-163">-SubscriptionId</span></span>
<span data-ttu-id="ca66c-164">Identyfikator subskrypcji źródłowej.</span><span class="sxs-lookup"><span data-stu-id="ca66c-164">Source subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, LongTermRetentionBackupRestoreParameter
Aliases: SourceSubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-165">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ca66c-165">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="ca66c-166">Nazwa docelowej bazy danych wystąpienia, do których ma zostać przywrócona.</span><span class="sxs-lookup"><span data-stu-id="ca66c-166">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="ca66c-167">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="ca66c-167">-TargetInstanceName</span></span>
<span data-ttu-id="ca66c-168">Nazwa wystąpienia docelowego, do których chcesz przywrócić dane.</span><span class="sxs-lookup"><span data-stu-id="ca66c-168">The name of the target instance to restore to.</span></span>
<span data-ttu-id="ca66c-169">Jeśli nie zostanie określone, wystąpienie docelowe będzie takie samo jak wystąpienie źródłowe.</span><span class="sxs-lookup"><span data-stu-id="ca66c-169">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-170">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca66c-170">-TargetResourceGroupName</span></span>
<span data-ttu-id="ca66c-171">Nazwa docelowej grupy zasobów, do których ma zostać przywrócona.</span><span class="sxs-lookup"><span data-stu-id="ca66c-171">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="ca66c-172">Jeśli nie zostanie określona, docelowa grupa zasobów jest taka sama jak grupa zasobów źródłowych.</span><span class="sxs-lookup"><span data-stu-id="ca66c-172">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca66c-173">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca66c-173">-Confirm</span></span>
<span data-ttu-id="ca66c-174">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ca66c-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca66c-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca66c-175">-WhatIf</span></span>
<span data-ttu-id="ca66c-176">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca66c-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca66c-177">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ca66c-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca66c-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca66c-178">CommonParameters</span></span>
<span data-ttu-id="ca66c-179">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca66c-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca66c-180">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca66c-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca66c-181">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca66c-181">INPUTS</span></span>

### <span data-ttu-id="ca66c-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ca66c-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="ca66c-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ca66c-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="ca66c-184">System.String</span><span class="sxs-lookup"><span data-stu-id="ca66c-184">System.String</span></span>

## <span data-ttu-id="ca66c-185">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca66c-185">OUTPUTS</span></span>

### <span data-ttu-id="ca66c-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ca66c-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ca66c-187">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca66c-187">NOTES</span></span>

## <span data-ttu-id="ca66c-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca66c-188">RELATED LINKS</span></span>
