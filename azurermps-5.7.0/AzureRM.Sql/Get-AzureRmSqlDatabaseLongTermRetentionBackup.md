---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: da3b47923f39e6910566a210ddbd325d9da76ca7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524849"
---
# <span data-ttu-id="fac1b-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fac1b-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="fac1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fac1b-102">SYNOPSIS</span></span>
<span data-ttu-id="fac1b-103">Pobiera co najmniej jedno długoterminowe kopie zapasowe przechowywania.</span><span class="sxs-lookup"><span data-stu-id="fac1b-103">Gets one or more long term retention backups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fac1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fac1b-104">SYNTAX</span></span>

### <span data-ttu-id="fac1b-105">Lokalizacja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fac1b-105">Location (Default)</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fac1b-106">Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fac1b-106">ServerName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [[-DatabaseName] <String>] [-OnlyLatestPerDatabase] [[-DatabaseState] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac1b-107">Backupname</span><span class="sxs-lookup"><span data-stu-id="fac1b-107">BackupName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac1b-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="fac1b-108">GetBackupByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac1b-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="fac1b-109">GetBackupsByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String>
 [-OnlyLatestPerDatabase] [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac1b-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="fac1b-110">GetBackupByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac1b-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="fac1b-111">GetBackupsByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fac1b-112">Opis</span><span class="sxs-lookup"><span data-stu-id="fac1b-112">DESCRIPTION</span></span>
<span data-ttu-id="fac1b-113">Polecenie cmdlet **Get-AzureRmSqlDatabaseLongTermRetentionBackup** pobiera wszystkie długotrwałe kopie zapasowe przechowywania dla lokalizacji, serwera lub bazy danych albo pobiera określoną długotrwałą kopię zapasową przechowywania.</span><span class="sxs-lookup"><span data-stu-id="fac1b-113">The **Get-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="fac1b-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fac1b-114">EXAMPLES</span></span>

### <span data-ttu-id="fac1b-115">Przykład 1. pobieranie wszystkich kopii zapasowych dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="fac1b-115">Example 1: Get all backups for a location</span></span>
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

<span data-ttu-id="fac1b-116">To polecenie pobiera wszystkie długie kopie zapasowe przechowywania dla wszystkich baz danych (które mogą być aktywne lub usunięte) w northeurope.</span><span class="sxs-lookup"><span data-stu-id="fac1b-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="fac1b-117">Przykład 2: pobieranie konkretnej kopii zapasowej przechowywania w długim okresie</span><span class="sxs-lookup"><span data-stu-id="fac1b-117">Example 2: Get a specific long term retention backup</span></span>
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

<span data-ttu-id="fac1b-118">To polecenie pobiera kopię zapasową przy użyciu nazwy 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="fac1b-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="fac1b-119">Przykład 3: pobieranie wszystkich długoterminowych kopii zapasowych przechowywania dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="fac1b-119">Example 3: Get all long term retention backups for a database</span></span>
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

<span data-ttu-id="fac1b-120">To polecenie pobiera wszystkie kopie zapasowe długotrwałego przechowywania dla database01</span><span class="sxs-lookup"><span data-stu-id="fac1b-120">This command gets all long term retention backups for database01</span></span>

## <span data-ttu-id="fac1b-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fac1b-121">PARAMETERS</span></span>

### <span data-ttu-id="fac1b-122">-Backupname</span><span class="sxs-lookup"><span data-stu-id="fac1b-122">-BackupName</span></span>
<span data-ttu-id="fac1b-123">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fac1b-123">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac1b-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fac1b-124">-DatabaseName</span></span>
<span data-ttu-id="fac1b-125">Nazwa bazy danych SQL Azure, z której pochodzi kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="fac1b-125">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: ServerName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac1b-126">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="fac1b-126">-DatabaseState</span></span>
<span data-ttu-id="fac1b-127">Stan bazy danych, której kopie zapasowe mają być wyszukiwane, aktywne, usunięte lub wszystkie.</span><span class="sxs-lookup"><span data-stu-id="fac1b-127">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="fac1b-128">Domyślnie wszystkie</span><span class="sxs-lookup"><span data-stu-id="fac1b-128">Defaults to All</span></span>

```yaml
Type: String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac1b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac1b-129">-DefaultProfile</span></span>
<span data-ttu-id="fac1b-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fac1b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fac1b-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fac1b-131">-InputObject</span></span>
<span data-ttu-id="fac1b-132">Obiekt bazy danych, dla którego mają zostać utworzone kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="fac1b-132">The database object to get backups for.</span></span>

```yaml
Type: AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fac1b-133">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fac1b-133">-Location</span></span>
<span data-ttu-id="fac1b-134">Lokalizacja serwera źródłowego kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="fac1b-134">The location of the backups' source server.</span></span>

```yaml
Type: String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac1b-135">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="fac1b-135">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="fac1b-136">Czy tylko uzyskać najnowszą kopię zapasową na bazę danych.</span><span class="sxs-lookup"><span data-stu-id="fac1b-136">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="fac1b-137">Wartość domyślna to FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="fac1b-137">Defaults to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac1b-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fac1b-138">-ResourceId</span></span>
<span data-ttu-id="fac1b-139">Identyfikator zasobu bazy danych, dla którego mają zostać utworzone kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="fac1b-139">The database Resource ID to get backups for.</span></span>

```yaml
Type: String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac1b-140">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fac1b-140">-ServerName</span></span>
<span data-ttu-id="fac1b-141">Nazwa programu Azure SQL Server, w którym znajdują się kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="fac1b-141">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac1b-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fac1b-142">-Confirm</span></span>
<span data-ttu-id="fac1b-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fac1b-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac1b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fac1b-144">-WhatIf</span></span>
<span data-ttu-id="fac1b-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fac1b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fac1b-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fac1b-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac1b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac1b-147">CommonParameters</span></span>
<span data-ttu-id="fac1b-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fac1b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fac1b-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fac1b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac1b-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fac1b-150">INPUTS</span></span>

### <span data-ttu-id="fac1b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="fac1b-151">System.String</span></span>
<span data-ttu-id="fac1b-152">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fac1b-152">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fac1b-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fac1b-153">OUTPUTS</span></span>

### <span data-ttu-id="fac1b-154">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="fac1b-154">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="fac1b-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fac1b-155">NOTES</span></span>

## <span data-ttu-id="fac1b-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fac1b-156">RELATED LINKS</span></span>

[<span data-ttu-id="fac1b-157">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fac1b-157">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="fac1b-158">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fac1b-158">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fac1b-159">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fac1b-159">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fac1b-160">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fac1b-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
