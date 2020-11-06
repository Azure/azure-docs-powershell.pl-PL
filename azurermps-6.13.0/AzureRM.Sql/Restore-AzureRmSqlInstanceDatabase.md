---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 61fe76eba8d1f8faf0ab45d0a24f56a8dabf3641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553419"
---
# <span data-ttu-id="23521-101">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="23521-101">Restore-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="23521-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23521-102">SYNOPSIS</span></span>
<span data-ttu-id="23521-103">Przywraca bazę danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="23521-103">Restores an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23521-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23521-104">SYNTAX</span></span>

### <span data-ttu-id="23521-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="23521-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23521-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="23521-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23521-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="23521-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23521-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="23521-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23521-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="23521-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23521-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="23521-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23521-111">Opis</span><span class="sxs-lookup"><span data-stu-id="23521-111">DESCRIPTION</span></span>
<span data-ttu-id="23521-112">Polecenie cmdlet **Restore-AzureRmSqlInstanceDatabase** przywraca bazę danych wystąpienia od punktu w czasie w bazie danych na żywo.</span><span class="sxs-lookup"><span data-stu-id="23521-112">The **Restore-AzureRmSqlInstanceDatabase** cmdlet restores an instance database from a point in time in a live database.</span></span>
<span data-ttu-id="23521-113">Przywrócona baza danych zostanie utworzona jako nowa baza danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="23521-113">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="23521-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23521-114">EXAMPLES</span></span>

### <span data-ttu-id="23521-115">Przykład 1: Przywracanie bazy danych wystąpienia z punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="23521-115">Example 1: Restore a instance database from a point in time</span></span>
```
PS C:\> Restore-AzureRmSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="23521-116">Polecenie przywraca bazę danych wystąpienia Database01 z określonego czasu utworzenia kopii zapasowej do bazy danych wystąpienia o nazwie Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="23521-116">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="23521-117">Przykład 2: Przywracanie bazy danych wystąpienia z punktu w czasie do innego wystąpienia w innej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="23521-117">Example 2: Restore a instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="23521-118">Polecenie przywraca bazę danych wystąpienia Database01 na wystąpieniu managedInstance1 w grupie zasobów ResourceGroup01 z określonego momentu kopii zapasowej do bazy danych wystąpienia o nazwie Database01_restored w wystąpieniu managedInstance2 w grupie zasobów ResourceGroup02.</span><span class="sxs-lookup"><span data-stu-id="23521-118">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

## <span data-ttu-id="23521-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23521-119">PARAMETERS</span></span>

### <span data-ttu-id="23521-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23521-120">-AsJob</span></span>
<span data-ttu-id="23521-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="23521-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23521-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23521-122">-DefaultProfile</span></span>
<span data-ttu-id="23521-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23521-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23521-124">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="23521-124">-FromPointInTimeBackup</span></span>
<span data-ttu-id="23521-125">Przywracanie z kopii zapasowej w czasie.</span><span class="sxs-lookup"><span data-stu-id="23521-125">Restore from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23521-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23521-126">-InputObject</span></span>
<span data-ttu-id="23521-127">Obiekt bazy danych wystąpienia do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="23521-127">The Instance Database object to restore</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23521-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="23521-128">-InstanceName</span></span>
<span data-ttu-id="23521-129">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="23521-129">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23521-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23521-130">-Name</span></span>
<span data-ttu-id="23521-131">Nazwa bazy danych wystąpienia do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="23521-131">The instance database name to restore.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23521-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="23521-132">-PointInTime</span></span>
<span data-ttu-id="23521-133">Punkt w czasie, w którym ma zostać przywrócona baza danych.</span><span class="sxs-lookup"><span data-stu-id="23521-133">The point in time to restore the database to.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23521-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23521-134">-ResourceGroupName</span></span>
<span data-ttu-id="23521-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23521-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23521-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23521-136">-ResourceId</span></span>
<span data-ttu-id="23521-137">Identyfikator zasobu wystąpienia obiektu bazy danych, który ma zostać przywrócony</span><span class="sxs-lookup"><span data-stu-id="23521-137">The resource id of Instance Database object to restore</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23521-138">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="23521-138">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="23521-139">Nazwa docelowej bazy danych wystąpienia, do której ma zostać przywrócona operacja.</span><span class="sxs-lookup"><span data-stu-id="23521-139">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="23521-140">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="23521-140">-TargetInstanceName</span></span>
<span data-ttu-id="23521-141">Nazwa docelowego wystąpienia do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="23521-141">The name of the target instance to restore to.</span></span>
<span data-ttu-id="23521-142">Jeśli argument nie zostanie określony, wystąpienie docelowe jest takie samo jak wystąpienie źródłowe.</span><span class="sxs-lookup"><span data-stu-id="23521-142">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23521-143">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23521-143">-TargetResourceGroupName</span></span>
<span data-ttu-id="23521-144">Nazwa docelowej grupy zasobów do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="23521-144">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="23521-145">Jeśli nie określono tej wartości, Grupa zasobów docelowych jest taka sama jak źródłowa Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="23521-145">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23521-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23521-146">-Confirm</span></span>
<span data-ttu-id="23521-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23521-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23521-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23521-148">-WhatIf</span></span>
<span data-ttu-id="23521-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23521-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23521-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23521-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23521-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23521-151">CommonParameters</span></span>
<span data-ttu-id="23521-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23521-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23521-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23521-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23521-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23521-154">INPUTS</span></span>

### <span data-ttu-id="23521-155">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="23521-155">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="23521-156">System. String</span><span class="sxs-lookup"><span data-stu-id="23521-156">System.String</span></span>

## <span data-ttu-id="23521-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23521-157">OUTPUTS</span></span>

### <span data-ttu-id="23521-158">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="23521-158">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="23521-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23521-159">NOTES</span></span>

## <span data-ttu-id="23521-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23521-160">RELATED LINKS</span></span>
