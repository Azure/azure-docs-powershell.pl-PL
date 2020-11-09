---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e97143f282bc01bbdd9c5d6186f0ccb5532b1df1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318804"
---
# <span data-ttu-id="15da7-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="15da7-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="15da7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15da7-102">SYNOPSIS</span></span>
<span data-ttu-id="15da7-103">Pobiera co najmniej jedno długoterminowe kopie zapasowe przechowywania.</span><span class="sxs-lookup"><span data-stu-id="15da7-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="15da7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15da7-104">SYNTAX</span></span>

### <span data-ttu-id="15da7-105">Lokalizacja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="15da7-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15da7-106">Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="15da7-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15da7-107">Backupname</span><span class="sxs-lookup"><span data-stu-id="15da7-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15da7-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="15da7-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15da7-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="15da7-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15da7-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="15da7-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15da7-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="15da7-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15da7-112">Opis</span><span class="sxs-lookup"><span data-stu-id="15da7-112">DESCRIPTION</span></span>
<span data-ttu-id="15da7-113">Polecenie cmdlet **Get-AzSqlDatabaseLongTermRetentionBackup** pobiera wszystkie długotrwałe kopie zapasowe przechowywania dla lokalizacji, serwera lub bazy danych albo pobiera określoną długotrwałą kopię zapasową przechowywania.</span><span class="sxs-lookup"><span data-stu-id="15da7-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="15da7-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15da7-114">EXAMPLES</span></span>

### <span data-ttu-id="15da7-115">Przykład 1. pobieranie wszystkich kopii zapasowych dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="15da7-115">Example 1: Get all backups for a location</span></span>
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

<span data-ttu-id="15da7-116">To polecenie pobiera wszystkie długoterminowe kopie zapasowe przechowywania dla wszystkich baz danych (które mogą być aktywne lub usunięte) w northeurope, Grupa zasobów zostanie ustawiona tylko wtedy, gdy serwer jest na żywo.</span><span class="sxs-lookup"><span data-stu-id="15da7-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="15da7-117">Przykład 2: pobieranie wszystkich kopii zapasowych dla lokalizacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="15da7-117">Example 2: Get all backups for a location under a resource group</span></span>
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

<span data-ttu-id="15da7-118">To polecenie pobiera wszystkie długoterminowe kopie zapasowe przechowywania dla wszystkich baz danych (które mogą być aktywne lub usunięte) w grupie zasobów w northeurope.</span><span class="sxs-lookup"><span data-stu-id="15da7-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="15da7-119">Przykład 3: pobieranie konkretnej kopii zapasowej przechowywania w długim czasie</span><span class="sxs-lookup"><span data-stu-id="15da7-119">Example 3: Get a specific long term retention backup</span></span>
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

<span data-ttu-id="15da7-120">To polecenie pobiera kopię zapasową przy użyciu nazwy 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="15da7-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="15da7-121">Przykład 4: pobieranie wszystkich długoterminowych kopii zapasowych przechowywania dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="15da7-121">Example 4: Get all long term retention backups for a database</span></span>
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

<span data-ttu-id="15da7-122">To polecenie pobiera wszystkie kopie zapasowe długotrwałego przechowywania dla database01</span><span class="sxs-lookup"><span data-stu-id="15da7-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="15da7-123">Przykład 5: pobieranie kopii zapasowych w długim okresie przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="15da7-123">Example 5: Get long term retention backups using filtering</span></span>
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

<span data-ttu-id="15da7-124">To polecenie pobiera wszystkie kopie zapasowe o nazwie rozpoczynającej się od tekstu "601061b7".</span><span class="sxs-lookup"><span data-stu-id="15da7-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="15da7-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15da7-125">PARAMETERS</span></span>

### <span data-ttu-id="15da7-126">-Backupname</span><span class="sxs-lookup"><span data-stu-id="15da7-126">-BackupName</span></span>
<span data-ttu-id="15da7-127">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="15da7-127">The name of the backup.</span></span>

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

### <span data-ttu-id="15da7-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="15da7-128">-DatabaseName</span></span>
<span data-ttu-id="15da7-129">Nazwa bazy danych SQL Azure, z której pochodzi kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="15da7-129">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="15da7-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="15da7-130">-DatabaseState</span></span>
<span data-ttu-id="15da7-131">Stan bazy danych, której kopie zapasowe mają być wyszukiwane, aktywne, usunięte lub wszystkie.</span><span class="sxs-lookup"><span data-stu-id="15da7-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="15da7-132">Domyślnie wszystkie</span><span class="sxs-lookup"><span data-stu-id="15da7-132">Defaults to All</span></span>

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

### <span data-ttu-id="15da7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15da7-133">-DefaultProfile</span></span>
<span data-ttu-id="15da7-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15da7-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15da7-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="15da7-135">-InputObject</span></span>
<span data-ttu-id="15da7-136">Obiekt bazy danych, dla którego mają zostać utworzone kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="15da7-136">The database object to get backups for.</span></span>

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

### <span data-ttu-id="15da7-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="15da7-137">-Location</span></span>
<span data-ttu-id="15da7-138">Lokalizacja serwera źródłowego kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="15da7-138">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="15da7-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="15da7-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="15da7-140">Czy tylko uzyskać najnowszą kopię zapasową na bazę danych.</span><span class="sxs-lookup"><span data-stu-id="15da7-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="15da7-141">Wartość domyślna to FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="15da7-141">Defaults to false.</span></span>

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

### <span data-ttu-id="15da7-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15da7-142">-ResourceGroupName</span></span>
<span data-ttu-id="15da7-143">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="15da7-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="15da7-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15da7-144">-ResourceId</span></span>
<span data-ttu-id="15da7-145">Identyfikator zasobu bazy danych, dla którego mają zostać utworzone kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="15da7-145">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="15da7-146">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="15da7-146">-ServerName</span></span>
<span data-ttu-id="15da7-147">Nazwa programu Azure SQL Server, w którym znajdują się kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="15da7-147">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="15da7-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15da7-148">-Confirm</span></span>
<span data-ttu-id="15da7-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15da7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15da7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15da7-150">-WhatIf</span></span>
<span data-ttu-id="15da7-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15da7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15da7-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15da7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15da7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15da7-153">CommonParameters</span></span>
<span data-ttu-id="15da7-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15da7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15da7-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15da7-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15da7-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15da7-156">INPUTS</span></span>

### <span data-ttu-id="15da7-157">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="15da7-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="15da7-158">System. String</span><span class="sxs-lookup"><span data-stu-id="15da7-158">System.String</span></span>

## <span data-ttu-id="15da7-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15da7-159">OUTPUTS</span></span>

### <span data-ttu-id="15da7-160">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="15da7-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="15da7-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15da7-161">NOTES</span></span>

## <span data-ttu-id="15da7-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15da7-162">RELATED LINKS</span></span>

[<span data-ttu-id="15da7-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="15da7-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="15da7-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="15da7-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="15da7-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="15da7-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="15da7-166">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="15da7-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)