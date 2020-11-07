---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: d513c186f621329510582c9cd69a64461f9e068f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707778"
---
# <span data-ttu-id="a96a9-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a96a9-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="a96a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a96a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a96a9-103">Przywraca bazę danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a96a9-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="a96a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a96a9-104">SYNTAX</span></span>

### <span data-ttu-id="a96a9-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a96a9-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96a9-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="a96a9-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96a9-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a96a9-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a96a9-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="a96a9-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96a9-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="a96a9-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a96a9-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a96a9-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96a9-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a96a9-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96a9-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a96a9-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96a9-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="a96a9-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a96a9-114">Opis</span><span class="sxs-lookup"><span data-stu-id="a96a9-114">DESCRIPTION</span></span>
<span data-ttu-id="a96a9-115">Polecenie cmdlet **Restore-AzSqlInstanceDatabase** przywraca bazę danych wystąpienia z kopii zapasowej Geo-nadmiarowej lub punktu w czasie w bazie danych na żywo.</span><span class="sxs-lookup"><span data-stu-id="a96a9-115">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup or a point in time in a live database.</span></span>
<span data-ttu-id="a96a9-116">Przywrócona baza danych zostanie utworzona jako nowa baza danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a96a9-116">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="a96a9-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a96a9-117">EXAMPLES</span></span>

### <span data-ttu-id="a96a9-118">Przykład 1: Przywracanie bazy danych wystąpienia z punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="a96a9-118">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="a96a9-119">Polecenie przywraca bazę danych wystąpienia Database01 z określonego czasu utworzenia kopii zapasowej do bazy danych wystąpienia o nazwie Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="a96a9-119">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="a96a9-120">Przykład 2: Przywracanie bazy danych wystąpienia z punktu w czasie do innego wystąpienia w innej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a96a9-120">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="a96a9-121">Polecenie przywraca bazę danych wystąpienia Database01 na wystąpieniu managedInstance1 w grupie zasobów ResourceGroup01 z określonego momentu kopii zapasowej do bazy danych wystąpienia o nazwie Database01_restored w wystąpieniu managedInstance2 w grupie zasobów ResourceGroup02.</span><span class="sxs-lookup"><span data-stu-id="a96a9-121">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="a96a9-122">Przykład 3: Geo-Restore bazie danych wystąpienia</span><span class="sxs-lookup"><span data-stu-id="a96a9-122">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="a96a9-123">Pierwsze polecenie pobiera kopię zapasową Geo-nadmiarową bazy danych o nazwie Database01, a następnie zapisuje ją w zmiennej $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="a96a9-123">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="a96a9-124">Drugie polecenie przywraca kopię zapasową w $GeoBackup bazie danych wystąpienia o nazwie Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="a96a9-124">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

## <span data-ttu-id="a96a9-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a96a9-125">PARAMETERS</span></span>

### <span data-ttu-id="a96a9-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a96a9-126">-AsJob</span></span>
<span data-ttu-id="a96a9-127">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a96a9-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a96a9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96a9-128">-DefaultProfile</span></span>
<span data-ttu-id="a96a9-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a96a9-129">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="a96a9-130">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a96a9-130">-FromGeoBackup</span></span>
<span data-ttu-id="a96a9-131">Przywracanie z kopii zapasowej Geo.</span><span class="sxs-lookup"><span data-stu-id="a96a9-131">Restore from a geo backup.</span></span>

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

### <span data-ttu-id="a96a9-132">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="a96a9-132">-FromPointInTimeBackup</span></span>
<span data-ttu-id="a96a9-133">Przywracanie z kopii zapasowej w czasie.</span><span class="sxs-lookup"><span data-stu-id="a96a9-133">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96a9-134">-Moja kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="a96a9-134">-GeoBackupObject</span></span>
<span data-ttu-id="a96a9-135">Obiekt bazy danych odzyskiwalnej instancji do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="a96a9-135">The recoverable instance database object to restore</span></span>

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

### <span data-ttu-id="a96a9-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a96a9-136">-InputObject</span></span>
<span data-ttu-id="a96a9-137">Obiekt bazy danych wystąpienia do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="a96a9-137">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a96a9-138">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a96a9-138">-InstanceName</span></span>
<span data-ttu-id="a96a9-139">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a96a9-139">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96a9-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a96a9-140">-Name</span></span>
<span data-ttu-id="a96a9-141">Nazwa bazy danych wystąpienia do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="a96a9-141">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96a9-142">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="a96a9-142">-PointInTime</span></span>
<span data-ttu-id="a96a9-143">Punkt w czasie, w którym ma zostać przywrócona baza danych.</span><span class="sxs-lookup"><span data-stu-id="a96a9-143">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96a9-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a96a9-144">-ResourceGroupName</span></span>
<span data-ttu-id="a96a9-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a96a9-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96a9-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a96a9-146">-ResourceId</span></span>
<span data-ttu-id="a96a9-147">Identyfikator zasobu wystąpienia obiektu bazy danych, który ma zostać przywrócony</span><span class="sxs-lookup"><span data-stu-id="a96a9-147">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
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

### <span data-ttu-id="a96a9-148">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a96a9-148">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="a96a9-149">Nazwa docelowej bazy danych wystąpienia, do której ma zostać przywrócona operacja.</span><span class="sxs-lookup"><span data-stu-id="a96a9-149">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="a96a9-150">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="a96a9-150">-TargetInstanceName</span></span>
<span data-ttu-id="a96a9-151">Nazwa docelowego wystąpienia do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="a96a9-151">The name of the target instance to restore to.</span></span>
<span data-ttu-id="a96a9-152">Jeśli argument nie zostanie określony, wystąpienie docelowe jest takie samo jak wystąpienie źródłowe.</span><span class="sxs-lookup"><span data-stu-id="a96a9-152">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96a9-153">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a96a9-153">-TargetResourceGroupName</span></span>
<span data-ttu-id="a96a9-154">Nazwa docelowej grupy zasobów do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="a96a9-154">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="a96a9-155">Jeśli nie określono tej wartości, Grupa zasobów docelowych jest taka sama jak źródłowa Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="a96a9-155">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96a9-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a96a9-156">-Confirm</span></span>
<span data-ttu-id="a96a9-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a96a9-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a96a9-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a96a9-158">-WhatIf</span></span>
<span data-ttu-id="a96a9-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a96a9-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a96a9-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a96a9-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a96a9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96a9-161">CommonParameters</span></span>
<span data-ttu-id="a96a9-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a96a9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96a9-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a96a9-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96a9-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a96a9-164">INPUTS</span></span>

### <span data-ttu-id="a96a9-165">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a96a9-165">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="a96a9-166">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a96a9-166">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="a96a9-167">System. String</span><span class="sxs-lookup"><span data-stu-id="a96a9-167">System.String</span></span>

## <span data-ttu-id="a96a9-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a96a9-168">OUTPUTS</span></span>

### <span data-ttu-id="a96a9-169">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a96a9-169">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a96a9-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a96a9-170">NOTES</span></span>

## <span data-ttu-id="a96a9-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a96a9-171">RELATED LINKS</span></span>
