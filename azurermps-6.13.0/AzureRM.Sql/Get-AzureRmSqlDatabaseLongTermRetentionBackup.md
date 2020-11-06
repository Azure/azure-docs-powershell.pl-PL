---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 6ae416cd9ac49bc4d7f54289cd9c5b43a377d20b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544784"
---
# <span data-ttu-id="51e2b-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="51e2b-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="51e2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="51e2b-103">Pobiera co najmniej jedno długoterminowe kopie zapasowe przechowywania.</span><span class="sxs-lookup"><span data-stu-id="51e2b-103">Gets one or more long term retention backups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51e2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51e2b-104">SYNTAX</span></span>

### <span data-ttu-id="51e2b-105">Lokalizacja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="51e2b-105">Location (Default)</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e2b-106">Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="51e2b-106">ServerName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e2b-107">Backupname</span><span class="sxs-lookup"><span data-stu-id="51e2b-107">BackupName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 -DatabaseName <String> [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51e2b-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="51e2b-108">GetBackupByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e2b-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="51e2b-109">GetBackupsByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e2b-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="51e2b-110">GetBackupByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e2b-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="51e2b-111">GetBackupsByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51e2b-112">Opis</span><span class="sxs-lookup"><span data-stu-id="51e2b-112">DESCRIPTION</span></span>
<span data-ttu-id="51e2b-113">Polecenie cmdlet **Get-AzureRmSqlDatabaseLongTermRetentionBackup** pobiera wszystkie długotrwałe kopie zapasowe przechowywania dla lokalizacji, serwera lub bazy danych albo pobiera określoną długotrwałą kopię zapasową przechowywania.</span><span class="sxs-lookup"><span data-stu-id="51e2b-113">The **Get-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="51e2b-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51e2b-114">EXAMPLES</span></span>

### <span data-ttu-id="51e2b-115">Przykład 1. pobieranie wszystkich kopii zapasowych dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="51e2b-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope


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

<span data-ttu-id="51e2b-116">To polecenie pobiera wszystkie długie kopie zapasowe przechowywania dla wszystkich baz danych (które mogą być aktywne lub usunięte) w northeurope.</span><span class="sxs-lookup"><span data-stu-id="51e2b-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="51e2b-117">Przykład 2: pobieranie konkretnej kopii zapasowej przechowywania w długim okresie</span><span class="sxs-lookup"><span data-stu-id="51e2b-117">Example 2: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="51e2b-118">To polecenie pobiera kopię zapasową przy użyciu nazwy 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="51e2b-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="51e2b-119">Przykład 3: pobieranie wszystkich długoterminowych kopii zapasowych przechowywania dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="51e2b-119">Example 3: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzureRmSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="51e2b-120">To polecenie pobiera wszystkie kopie zapasowe długotrwałego przechowywania dla database01</span><span class="sxs-lookup"><span data-stu-id="51e2b-120">This command gets all long term retention backups for database01</span></span>

## <span data-ttu-id="51e2b-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51e2b-121">PARAMETERS</span></span>

### <span data-ttu-id="51e2b-122">-Backupname</span><span class="sxs-lookup"><span data-stu-id="51e2b-122">-BackupName</span></span>
<span data-ttu-id="51e2b-123">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="51e2b-123">The name of the backup.</span></span>

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

### <span data-ttu-id="51e2b-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="51e2b-124">-DatabaseName</span></span>
<span data-ttu-id="51e2b-125">Nazwa bazy danych SQL Azure, z której pochodzi kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="51e2b-125">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="51e2b-126">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="51e2b-126">-DatabaseState</span></span>
<span data-ttu-id="51e2b-127">Stan bazy danych, której kopie zapasowe mają być wyszukiwane, aktywne, usunięte lub wszystkie.</span><span class="sxs-lookup"><span data-stu-id="51e2b-127">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="51e2b-128">Domyślnie wszystkie</span><span class="sxs-lookup"><span data-stu-id="51e2b-128">Defaults to All</span></span>

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

### <span data-ttu-id="51e2b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e2b-129">-DefaultProfile</span></span>
<span data-ttu-id="51e2b-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51e2b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51e2b-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="51e2b-131">-InputObject</span></span>
<span data-ttu-id="51e2b-132">Obiekt bazy danych, dla którego mają zostać utworzone kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="51e2b-132">The database object to get backups for.</span></span>

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

### <span data-ttu-id="51e2b-133">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="51e2b-133">-Location</span></span>
<span data-ttu-id="51e2b-134">Lokalizacja serwera źródłowego kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="51e2b-134">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="51e2b-135">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="51e2b-135">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="51e2b-136">Czy tylko uzyskać najnowszą kopię zapasową na bazę danych.</span><span class="sxs-lookup"><span data-stu-id="51e2b-136">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="51e2b-137">Wartość domyślna to FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="51e2b-137">Defaults to false.</span></span>

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

### <span data-ttu-id="51e2b-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51e2b-138">-ResourceId</span></span>
<span data-ttu-id="51e2b-139">Identyfikator zasobu bazy danych, dla którego mają zostać utworzone kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="51e2b-139">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="51e2b-140">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="51e2b-140">-ServerName</span></span>
<span data-ttu-id="51e2b-141">Nazwa programu Azure SQL Server, w którym znajdują się kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="51e2b-141">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="51e2b-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51e2b-142">-Confirm</span></span>
<span data-ttu-id="51e2b-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51e2b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e2b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e2b-144">-WhatIf</span></span>
<span data-ttu-id="51e2b-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51e2b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e2b-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="51e2b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e2b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e2b-147">CommonParameters</span></span>
<span data-ttu-id="51e2b-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e2b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e2b-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51e2b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e2b-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51e2b-150">INPUTS</span></span>

### <span data-ttu-id="51e2b-151">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="51e2b-151">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>
<span data-ttu-id="51e2b-152">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="51e2b-152">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="51e2b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="51e2b-153">System.String</span></span>

## <span data-ttu-id="51e2b-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51e2b-154">OUTPUTS</span></span>

### <span data-ttu-id="51e2b-155">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="51e2b-155">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="51e2b-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51e2b-156">NOTES</span></span>

## <span data-ttu-id="51e2b-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51e2b-157">RELATED LINKS</span></span>

[<span data-ttu-id="51e2b-158">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="51e2b-158">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="51e2b-159">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="51e2b-159">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="51e2b-160">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="51e2b-160">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="51e2b-161">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="51e2b-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
