---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 68481d49fb37fb5246021fb8daa2d53a64b5c6b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548491"
---
# <span data-ttu-id="e5862-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e5862-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="e5862-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5862-102">SYNOPSIS</span></span>
<span data-ttu-id="e5862-103">Usuwa kopię zapasową długotrwałego przechowywania.</span><span class="sxs-lookup"><span data-stu-id="e5862-103">Deletes a long term retention backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5862-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5862-104">SYNTAX</span></span>

### <span data-ttu-id="e5862-105">RemoveBackupDefault (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e5862-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5862-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5862-106">RemoveBackupByInputObject</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5862-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5862-107">RemoveBackupByResourceId</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5862-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e5862-108">DESCRIPTION</span></span>
<span data-ttu-id="e5862-109">Polecenie cmdlet **Remove-AzureRmSqlDatabaseLongTermRetentionBackup** usuwa określoną kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="e5862-109">The **Remove-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="e5862-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5862-110">EXAMPLES</span></span>

### <span data-ttu-id="e5862-111">Przykład 1: Usuwanie jednej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="e5862-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="e5862-112">Usuwa kopię zapasową z nazwą 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="e5862-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="e5862-113">Przykład 2: Usuwanie wszystkich kopii zapasowych w lokalizacji</span><span class="sxs-lookup"><span data-stu-id="e5862-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzureRmSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="e5862-114">To polecenie usuwa wszystkie długotrwałe kopie zapasowe przechowywania dla lokalizacji northeurope.</span><span class="sxs-lookup"><span data-stu-id="e5862-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="e5862-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5862-115">PARAMETERS</span></span>

### <span data-ttu-id="e5862-116">-Backupname</span><span class="sxs-lookup"><span data-stu-id="e5862-116">-BackupName</span></span>
<span data-ttu-id="e5862-117">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e5862-117">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5862-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e5862-118">-DatabaseName</span></span>
<span data-ttu-id="e5862-119">Nazwa bazy danych SQL Azure, z której pochodzi kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="e5862-119">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5862-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5862-120">-DefaultProfile</span></span>
<span data-ttu-id="e5862-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5862-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5862-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e5862-122">-Force</span></span>
<span data-ttu-id="e5862-123">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="e5862-123">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5862-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5862-124">-InputObject</span></span>
<span data-ttu-id="e5862-125">Obiekt kopii zapasowej przechowywania długoterminowej bazy danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e5862-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5862-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e5862-126">-Location</span></span>
<span data-ttu-id="e5862-127">Lokalizacja serwera źródłowego kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="e5862-127">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5862-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5862-128">-ResourceId</span></span>
<span data-ttu-id="e5862-129">Identyfikator zasobu kopii zapasowej przechowywania długoterminowej bazy danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e5862-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5862-130">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e5862-130">-ServerName</span></span>
<span data-ttu-id="e5862-131">Nazwa programu Azure SQL Server, w którym znajduje się kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="e5862-131">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5862-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5862-132">-Confirm</span></span>
<span data-ttu-id="e5862-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5862-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5862-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5862-134">-WhatIf</span></span>
<span data-ttu-id="e5862-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5862-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5862-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5862-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5862-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5862-137">CommonParameters</span></span>
<span data-ttu-id="e5862-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5862-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5862-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5862-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5862-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5862-140">INPUTS</span></span>

### <span data-ttu-id="e5862-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e5862-141">System.String</span></span>

## <span data-ttu-id="e5862-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5862-142">OUTPUTS</span></span>

### <span data-ttu-id="e5862-143">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="e5862-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="e5862-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5862-144">NOTES</span></span>

## <span data-ttu-id="e5862-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5862-145">RELATED LINKS</span></span>

[<span data-ttu-id="e5862-146">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e5862-146">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="e5862-147">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5862-147">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="e5862-148">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5862-148">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="e5862-149">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e5862-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
