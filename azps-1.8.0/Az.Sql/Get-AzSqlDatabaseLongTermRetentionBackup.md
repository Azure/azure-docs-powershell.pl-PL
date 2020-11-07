---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 593a9c4764afd70003ee5c807be069eff977c6e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707989"
---
# <span data-ttu-id="8b936-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8b936-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="8b936-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b936-102">SYNOPSIS</span></span>
<span data-ttu-id="8b936-103">Pobiera co najmniej jedno długoterminowe kopie zapasowe przechowywania.</span><span class="sxs-lookup"><span data-stu-id="8b936-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="8b936-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b936-104">SYNTAX</span></span>

### <span data-ttu-id="8b936-105">Lokalizacja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8b936-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b936-106">Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8b936-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b936-107">Backupname</span><span class="sxs-lookup"><span data-stu-id="8b936-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b936-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b936-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b936-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b936-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b936-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b936-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b936-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b936-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b936-112">Opis</span><span class="sxs-lookup"><span data-stu-id="8b936-112">DESCRIPTION</span></span>
<span data-ttu-id="8b936-113">Polecenie cmdlet **Get-AzSqlDatabaseLongTermRetentionBackup** pobiera wszystkie długotrwałe kopie zapasowe przechowywania dla lokalizacji, serwera lub bazy danych albo pobiera określoną długotrwałą kopię zapasową przechowywania.</span><span class="sxs-lookup"><span data-stu-id="8b936-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="8b936-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b936-114">EXAMPLES</span></span>

### <span data-ttu-id="8b936-115">Przykład 1. pobieranie wszystkich kopii zapasowych dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="8b936-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="8b936-116">To polecenie pobiera wszystkie długie kopie zapasowe przechowywania dla wszystkich baz danych (które mogą być aktywne lub usunięte) w northeurope.</span><span class="sxs-lookup"><span data-stu-id="8b936-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="8b936-117">Przykład 2: pobieranie konkretnej kopii zapasowej przechowywania w długim okresie</span><span class="sxs-lookup"><span data-stu-id="8b936-117">Example 2: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="8b936-118">To polecenie pobiera kopię zapasową przy użyciu nazwy 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="8b936-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="8b936-119">Przykład 3: pobieranie wszystkich długoterminowych kopii zapasowych przechowywania dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="8b936-119">Example 3: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="8b936-120">To polecenie pobiera wszystkie kopie zapasowe długotrwałego przechowywania dla database01</span><span class="sxs-lookup"><span data-stu-id="8b936-120">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="8b936-121">Przykład 4: pobieranie kopii zapasowych przechowywania długoterminowego przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="8b936-121">Example 4: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="8b936-122">To polecenie pobiera wszystkie kopie zapasowe o nazwie rozpoczynającej się od tekstu "601061b7".</span><span class="sxs-lookup"><span data-stu-id="8b936-122">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="8b936-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b936-123">PARAMETERS</span></span>

### <span data-ttu-id="8b936-124">-Backupname</span><span class="sxs-lookup"><span data-stu-id="8b936-124">-BackupName</span></span>
<span data-ttu-id="8b936-125">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8b936-125">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8b936-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8b936-126">-DatabaseName</span></span>
<span data-ttu-id="8b936-127">Nazwa bazy danych SQL Azure, z której pochodzi kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="8b936-127">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="8b936-128">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="8b936-128">-DatabaseState</span></span>
<span data-ttu-id="8b936-129">Stan bazy danych, której kopie zapasowe mają być wyszukiwane, aktywne, usunięte lub wszystkie.</span><span class="sxs-lookup"><span data-stu-id="8b936-129">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="8b936-130">Domyślnie wszystkie</span><span class="sxs-lookup"><span data-stu-id="8b936-130">Defaults to All</span></span>

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

### <span data-ttu-id="8b936-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b936-131">-DefaultProfile</span></span>
<span data-ttu-id="8b936-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b936-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b936-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8b936-133">-InputObject</span></span>
<span data-ttu-id="8b936-134">Obiekt bazy danych, dla którego mają zostać utworzone kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="8b936-134">The database object to get backups for.</span></span>

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

### <span data-ttu-id="8b936-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8b936-135">-Location</span></span>
<span data-ttu-id="8b936-136">Lokalizacja serwera źródłowego kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="8b936-136">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="8b936-137">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="8b936-137">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="8b936-138">Czy tylko uzyskać najnowszą kopię zapasową na bazę danych.</span><span class="sxs-lookup"><span data-stu-id="8b936-138">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="8b936-139">Wartość domyślna to FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="8b936-139">Defaults to false.</span></span>

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

### <span data-ttu-id="8b936-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b936-140">-ResourceId</span></span>
<span data-ttu-id="8b936-141">Identyfikator zasobu bazy danych, dla którego mają zostać utworzone kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="8b936-141">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="8b936-142">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8b936-142">-ServerName</span></span>
<span data-ttu-id="8b936-143">Nazwa programu Azure SQL Server, w którym znajdują się kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="8b936-143">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="8b936-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b936-144">-Confirm</span></span>
<span data-ttu-id="8b936-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b936-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b936-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b936-146">-WhatIf</span></span>
<span data-ttu-id="8b936-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b936-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b936-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8b936-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b936-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b936-149">CommonParameters</span></span>
<span data-ttu-id="8b936-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b936-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b936-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b936-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b936-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b936-152">INPUTS</span></span>

### <span data-ttu-id="8b936-153">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8b936-153">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="8b936-154">System. String</span><span class="sxs-lookup"><span data-stu-id="8b936-154">System.String</span></span>

## <span data-ttu-id="8b936-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b936-155">OUTPUTS</span></span>

### <span data-ttu-id="8b936-156">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="8b936-156">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="8b936-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b936-157">NOTES</span></span>

## <span data-ttu-id="8b936-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b936-158">RELATED LINKS</span></span>

[<span data-ttu-id="8b936-159">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8b936-159">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8b936-160">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b936-160">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8b936-161">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b936-161">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8b936-162">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="8b936-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)