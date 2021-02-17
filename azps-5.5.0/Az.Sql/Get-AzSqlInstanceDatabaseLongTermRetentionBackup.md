---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: ccd716b493640afef7b5adea0b2e834c10893c3c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176922"
---
# <span data-ttu-id="6cc49-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6cc49-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="6cc49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cc49-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc49-103">Otrzymuje długookresowe kopie zapasowe przechowywania.</span><span class="sxs-lookup"><span data-stu-id="6cc49-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="6cc49-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6cc49-104">SYNTAX</span></span>

### <span data-ttu-id="6cc49-105">Lokalizacja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6cc49-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cc49-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="6cc49-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cc49-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cc49-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cc49-108">Nazwa_kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="6cc49-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cc49-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="6cc49-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cc49-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="6cc49-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cc49-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="6cc49-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cc49-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="6cc49-112">DESCRIPTION</span></span>
<span data-ttu-id="6cc49-113">{{ Wypełnij opis }}</span><span class="sxs-lookup"><span data-stu-id="6cc49-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="6cc49-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6cc49-114">EXAMPLES</span></span>

### <span data-ttu-id="6cc49-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6cc49-115">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


BackupExpirationTime : 3/10/2020 1:10:45 PM
BackupName           : 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
BackupTime           : 2/22/2020 6:04:15 AM
DatabaseName         : test
DatabaseDeletionTime : 2/24/2020 2:56:44 PM
Location             : southeastasia
ResourceId           : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManaged
                       Instances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
ManagedInstanceName  : testInstance
InstanceCreateTime   : 10/17/2019 4:52:10 PM
ResourceGroupName    : testResourceGroup
```

<span data-ttu-id="6cc49-116">Pobiera wszystkie długoterminowe kopie zapasowe przechowywania dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6cc49-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="6cc49-117">Grupa zasobów jest opcjonalna.</span><span class="sxs-lookup"><span data-stu-id="6cc49-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="6cc49-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cc49-118">PARAMETERS</span></span>

### <span data-ttu-id="6cc49-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="6cc49-119">-BackupName</span></span>
<span data-ttu-id="6cc49-120">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="6cc49-120">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc49-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cc49-121">-DatabaseName</span></span>
<span data-ttu-id="6cc49-122">Nazwa zarządzanej bazy danych, pod którym znajdują się kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="6cc49-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc49-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="6cc49-123">-DatabaseState</span></span>
<span data-ttu-id="6cc49-124">Stan bazy danych, której kopie zapasowe chcesz znaleźć, Żyj, Usunięte lub Wszystkie.</span><span class="sxs-lookup"><span data-stu-id="6cc49-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="6cc49-125">Domyślne ustawienie to Wszystko</span><span class="sxs-lookup"><span data-stu-id="6cc49-125">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc49-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc49-126">-DefaultProfile</span></span>
<span data-ttu-id="6cc49-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc49-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cc49-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cc49-128">-InputObject</span></span>
<span data-ttu-id="6cc49-129">Obiekt bazy danych do uzyskania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="6cc49-129">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc49-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6cc49-130">-InstanceName</span></span>
<span data-ttu-id="6cc49-131">Nazwa zarządzanego wystąpienia, pod którym znajdują się kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="6cc49-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc49-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6cc49-132">-Location</span></span>
<span data-ttu-id="6cc49-133">Lokalizacja źródłowego wystąpienia zarządzanego kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="6cc49-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc49-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="6cc49-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="6cc49-135">Czy chcesz uzyskać najnowszą kopię zapasową tylko dla 1 bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6cc49-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="6cc49-136">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="6cc49-136">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc49-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc49-137">-ResourceGroupName</span></span>
<span data-ttu-id="6cc49-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6cc49-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc49-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cc49-139">-ResourceId</span></span>
<span data-ttu-id="6cc49-140">Identyfikator zasobu bazy danych do uzyskania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="6cc49-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc49-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6cc49-141">-Confirm</span></span>
<span data-ttu-id="6cc49-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6cc49-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cc49-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc49-143">-WhatIf</span></span>
<span data-ttu-id="6cc49-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cc49-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cc49-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6cc49-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cc49-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc49-146">CommonParameters</span></span>
<span data-ttu-id="6cc49-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc49-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc49-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cc49-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc49-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cc49-149">INPUTS</span></span>

### <span data-ttu-id="6cc49-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6cc49-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="6cc49-151">System.String</span><span class="sxs-lookup"><span data-stu-id="6cc49-151">System.String</span></span>

## <span data-ttu-id="6cc49-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cc49-152">OUTPUTS</span></span>

### <span data-ttu-id="6cc49-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="6cc49-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="6cc49-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6cc49-154">NOTES</span></span>

## <span data-ttu-id="6cc49-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cc49-155">RELATED LINKS</span></span>

[<span data-ttu-id="6cc49-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6cc49-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="6cc49-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6cc49-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="6cc49-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6cc49-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="6cc49-159">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6cc49-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)