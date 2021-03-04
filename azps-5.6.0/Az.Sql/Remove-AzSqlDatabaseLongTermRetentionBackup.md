---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 01f9d475e678cee5b2fc131108a18bc5abec280d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957930"
---
# <span data-ttu-id="1b379-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="1b379-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="1b379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b379-102">SYNOPSIS</span></span>
<span data-ttu-id="1b379-103">Usuwa długookresową kopię zapasową przechowywania.</span><span class="sxs-lookup"><span data-stu-id="1b379-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="1b379-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1b379-104">SYNTAX</span></span>

### <span data-ttu-id="1b379-105">RemoveBackupDefault (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1b379-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b379-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="1b379-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b379-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b379-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b379-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1b379-108">DESCRIPTION</span></span>
<span data-ttu-id="1b379-109">Polecenie **cmdlet Remove-AzSqlDatabaseLongTermRetentionBackup** usuwa określoną kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="1b379-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="1b379-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1b379-110">EXAMPLES</span></span>

### <span data-ttu-id="1b379-111">Przykład 1. Usuwanie pojedynczej kopii zapasowej za pomocą grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1b379-111">Example 1: Delete a single backup with resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000" -ResourceGrouName resourcegroup01


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

<span data-ttu-id="1b379-112">Usuwa kopię zapasową o nazwie 601061b7-d10b-46e0-bf77-a2bfb16a6add;13165566550000000</span><span class="sxs-lookup"><span data-stu-id="1b379-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="1b379-113">Przykład 2. Usuwanie pojedynczej kopii zapasowej bez grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1b379-113">Example 2: Delete a single backup without resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server02 -DatabaseName database02 -BackupName "55970792-164c-4a4a-88e5-7158d092d503;131656309980000000"


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

<span data-ttu-id="1b379-114">Usuwa kopię zapasową o nazwie 601061b7-d10b-46e0-bf77-a2bfb16a6add;13165566550000000</span><span class="sxs-lookup"><span data-stu-id="1b379-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="1b379-115">Przykład 3. Usuwanie wszystkich kopii zapasowych dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="1b379-115">Example 3: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="1b379-116">To polecenie usuwa wszystkie długoterminowe kopie zapasowe przechowywania dla lokalizacji Northeurope.</span><span class="sxs-lookup"><span data-stu-id="1b379-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="1b379-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b379-117">PARAMETERS</span></span>

### <span data-ttu-id="1b379-118">-BackupName</span><span class="sxs-lookup"><span data-stu-id="1b379-118">-BackupName</span></span>
<span data-ttu-id="1b379-119">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="1b379-119">The name of the backup.</span></span>

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

### <span data-ttu-id="1b379-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b379-120">-DatabaseName</span></span>
<span data-ttu-id="1b379-121">Nazwa bazy danych Azure SQL Database, z których pochodzi kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="1b379-121">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="1b379-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b379-122">-DefaultProfile</span></span>
<span data-ttu-id="1b379-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b379-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b379-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1b379-124">-Force</span></span>
<span data-ttu-id="1b379-125">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="1b379-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1b379-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b379-126">-InputObject</span></span>
<span data-ttu-id="1b379-127">Obiekt długookresowej kopii zapasowej przechowywania bazy danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1b379-127">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b379-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1b379-128">-Location</span></span>
<span data-ttu-id="1b379-129">Lokalizacja serwera źródłowego kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="1b379-129">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="1b379-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b379-130">-ResourceGroupName</span></span>
<span data-ttu-id="1b379-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1b379-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b379-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b379-132">-ResourceId</span></span>
<span data-ttu-id="1b379-133">Identyfikator zasobu kopii zapasowej przechowywania długoterminowego bazy danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1b379-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="1b379-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1b379-134">-ServerName</span></span>
<span data-ttu-id="1b379-135">Nazwa serwera Azure SQL Server kopii zapasowej znajduje się poniżej.</span><span class="sxs-lookup"><span data-stu-id="1b379-135">The name of the Azure SQL Server the backup is under.</span></span>

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

### <span data-ttu-id="1b379-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b379-136">-Confirm</span></span>
<span data-ttu-id="1b379-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1b379-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b379-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b379-138">-WhatIf</span></span>
<span data-ttu-id="1b379-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b379-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b379-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1b379-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b379-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b379-141">CommonParameters</span></span>
<span data-ttu-id="1b379-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b379-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b379-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b379-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b379-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b379-144">INPUTS</span></span>

### <span data-ttu-id="1b379-145">System.String</span><span class="sxs-lookup"><span data-stu-id="1b379-145">System.String</span></span>

## <span data-ttu-id="1b379-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b379-146">OUTPUTS</span></span>

### <span data-ttu-id="1b379-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="1b379-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="1b379-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1b379-148">NOTES</span></span>

## <span data-ttu-id="1b379-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b379-149">RELATED LINKS</span></span>

[<span data-ttu-id="1b379-150">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="1b379-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="1b379-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b379-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="1b379-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b379-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="1b379-153">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1b379-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)