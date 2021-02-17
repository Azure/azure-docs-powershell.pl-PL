---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e97143f282bc01bbdd9c5d6186f0ccb5532b1df1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176978"
---
# <span data-ttu-id="5da10-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="5da10-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="5da10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5da10-102">SYNOPSIS</span></span>
<span data-ttu-id="5da10-103">Pobiera jedną lub więcej długoterminowych kopii zapasowych przechowywania.</span><span class="sxs-lookup"><span data-stu-id="5da10-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="5da10-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5da10-104">SYNTAX</span></span>

### <span data-ttu-id="5da10-105">Lokalizacja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="5da10-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5da10-106">ServerName</span><span class="sxs-lookup"><span data-stu-id="5da10-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5da10-107">Nazwa_kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="5da10-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5da10-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="5da10-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5da10-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="5da10-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5da10-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="5da10-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5da10-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="5da10-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5da10-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="5da10-112">DESCRIPTION</span></span>
<span data-ttu-id="5da10-113">Polecenie cmdlet **Get-AzSqlDatabaseLongTermRetentionBackup** pobiera wszystkie długookresowe kopie zapasowe przechowywania dla lokalizacji, serwera lub bazy danych albo pobiera określoną, długookresową kopię zapasową przechowywania.</span><span class="sxs-lookup"><span data-stu-id="5da10-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="5da10-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5da10-114">EXAMPLES</span></span>

### <span data-ttu-id="5da10-115">Przykład 1. Uzyskiwanie wszystkich kopii zapasowych dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="5da10-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="5da10-116">To polecenie pobiera wszystkie długoterminowe kopie zapasowe przechowywania dla wszystkich baz danych (które mogą być aktywne lub usunięte) w northeurope, grupa zasobów będzie ustawiana tylko wtedy, gdy serwer jest na żywo.</span><span class="sxs-lookup"><span data-stu-id="5da10-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="5da10-117">Przykład 2. Uzyskiwanie wszystkich kopii zapasowych dla lokalizacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="5da10-117">Example 2: Get all backups for a location under a resource group</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ResourceGroup resourceGroup01


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="5da10-118">To polecenie pobiera wszystkie długoterminowe kopie zapasowe przechowywania dla wszystkich baz danych (które mogą być ożywione lub usunięte) w grupie zasobów w Northeurope.</span><span class="sxs-lookup"><span data-stu-id="5da10-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="5da10-119">Przykład 3. Uzyskiwanie określonej, długookresowej kopii zapasowej przechowywania</span><span class="sxs-lookup"><span data-stu-id="5da10-119">Example 3: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="5da10-120">To polecenie pobiera kopię zapasową o nazwie 601061b7-d10b-46e0-bf77-a2bfb16a6add;13165566550000000</span><span class="sxs-lookup"><span data-stu-id="5da10-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="5da10-121">Przykład 4. Uzyskiwanie wszystkich długoterminowych kopii zapasowych przechowywania bazy danych</span><span class="sxs-lookup"><span data-stu-id="5da10-121">Example 4: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="5da10-122">To polecenie pobiera wszystkie długoterminowe kopie zapasowe przechowywania dla bazy danych 01</span><span class="sxs-lookup"><span data-stu-id="5da10-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="5da10-123">Przykład 5. Uzyskiwanie długoterminowych kopii zapasowych przechowywania przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="5da10-123">Example 5: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server01
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="5da10-124">To polecenie pobiera wszystkie kopie zapasowe o nazwie, która zaczyna się od "601061b7"</span><span class="sxs-lookup"><span data-stu-id="5da10-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="5da10-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5da10-125">PARAMETERS</span></span>

### <span data-ttu-id="5da10-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="5da10-126">-BackupName</span></span>
<span data-ttu-id="5da10-127">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="5da10-127">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da10-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5da10-128">-DatabaseName</span></span>
<span data-ttu-id="5da10-129">Nazwa bazy danych Azure SQL Database, z których pochodzi kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="5da10-129">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BackupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da10-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="5da10-130">-DatabaseState</span></span>
<span data-ttu-id="5da10-131">Stan bazy danych, której kopie zapasowe chcesz znaleźć, Żyj, Usunięte lub Wszystkie.</span><span class="sxs-lookup"><span data-stu-id="5da10-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="5da10-132">Domyślne ustawienie to Wszystko</span><span class="sxs-lookup"><span data-stu-id="5da10-132">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da10-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da10-133">-DefaultProfile</span></span>
<span data-ttu-id="5da10-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5da10-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5da10-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5da10-135">-InputObject</span></span>
<span data-ttu-id="5da10-136">Obiekt bazy danych do uzyskania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="5da10-136">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5da10-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5da10-137">-Location</span></span>
<span data-ttu-id="5da10-138">Lokalizacja serwera źródłowego kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="5da10-138">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da10-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="5da10-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="5da10-140">Czy chcesz uzyskać najnowszą kopię zapasową tylko dla 1 bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5da10-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="5da10-141">Wartość domyślna to false( fałsz).</span><span class="sxs-lookup"><span data-stu-id="5da10-141">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da10-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da10-142">-ResourceGroupName</span></span>
<span data-ttu-id="5da10-143">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5da10-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da10-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5da10-144">-ResourceId</span></span>
<span data-ttu-id="5da10-145">Identyfikator zasobu bazy danych do uzyskania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="5da10-145">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da10-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5da10-146">-ServerName</span></span>
<span data-ttu-id="5da10-147">Nazwa serwera Azure SQL Server, pod którym znajdują się kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="5da10-147">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da10-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5da10-148">-Confirm</span></span>
<span data-ttu-id="5da10-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5da10-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5da10-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5da10-150">-WhatIf</span></span>
<span data-ttu-id="5da10-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5da10-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5da10-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5da10-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5da10-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da10-153">CommonParameters</span></span>
<span data-ttu-id="5da10-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da10-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da10-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5da10-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da10-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5da10-156">INPUTS</span></span>

### <span data-ttu-id="5da10-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5da10-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="5da10-158">System.String</span><span class="sxs-lookup"><span data-stu-id="5da10-158">System.String</span></span>

## <span data-ttu-id="5da10-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5da10-159">OUTPUTS</span></span>

### <span data-ttu-id="5da10-160">Microsoft.Azure.Commands.sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="5da10-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="5da10-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5da10-161">NOTES</span></span>

## <span data-ttu-id="5da10-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5da10-162">RELATED LINKS</span></span>

[<span data-ttu-id="5da10-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="5da10-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="5da10-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5da10-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="5da10-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5da10-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="5da10-166">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5da10-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)