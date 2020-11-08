---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 9408e51cfcdab3cd2c82617ee7f8cb9bc7d3918a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053242"
---
# <span data-ttu-id="2eb05-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2eb05-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="2eb05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2eb05-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb05-103">Wykonywanie kopii zapasowych w długim czasie przechowywania.</span><span class="sxs-lookup"><span data-stu-id="2eb05-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="2eb05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2eb05-104">SYNTAX</span></span>

### <span data-ttu-id="2eb05-105">Lokalizacja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2eb05-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb05-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="2eb05-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb05-107">Bazy</span><span class="sxs-lookup"><span data-stu-id="2eb05-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb05-108">Backupname</span><span class="sxs-lookup"><span data-stu-id="2eb05-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb05-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb05-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb05-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="2eb05-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb05-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="2eb05-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb05-112">Opis</span><span class="sxs-lookup"><span data-stu-id="2eb05-112">DESCRIPTION</span></span>
<span data-ttu-id="2eb05-113">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="2eb05-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="2eb05-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2eb05-114">EXAMPLES</span></span>

### <span data-ttu-id="2eb05-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2eb05-115">Example 1</span></span>
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

<span data-ttu-id="2eb05-116">Pobiera wszystkie długoterminowe kopie zapasowe przechowywania dla konkretnej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2eb05-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="2eb05-117">Grupa zasobów jest opcjonalna.</span><span class="sxs-lookup"><span data-stu-id="2eb05-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="2eb05-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2eb05-118">PARAMETERS</span></span>

### <span data-ttu-id="2eb05-119">-Backupname</span><span class="sxs-lookup"><span data-stu-id="2eb05-119">-BackupName</span></span>
<span data-ttu-id="2eb05-120">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2eb05-120">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb05-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2eb05-121">-DatabaseName</span></span>
<span data-ttu-id="2eb05-122">Nazwa zarządzanej bazy danych, w której znajdują się kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="2eb05-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb05-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="2eb05-123">-DatabaseState</span></span>
<span data-ttu-id="2eb05-124">Stan bazy danych, której kopie zapasowe mają być wyszukiwane, aktywne, usunięte lub wszystkie.</span><span class="sxs-lookup"><span data-stu-id="2eb05-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="2eb05-125">Domyślnie wszystkie</span><span class="sxs-lookup"><span data-stu-id="2eb05-125">Defaults to All</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb05-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb05-126">-DefaultProfile</span></span>
<span data-ttu-id="2eb05-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb05-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb05-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2eb05-128">-InputObject</span></span>
<span data-ttu-id="2eb05-129">Obiekt bazy danych, dla którego mają zostać utworzone kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="2eb05-129">The database object to get backups for.</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb05-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2eb05-130">-InstanceName</span></span>
<span data-ttu-id="2eb05-131">Nazwa wystąpienia zarządzanego, w którym znajdują się kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="2eb05-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb05-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2eb05-132">-Location</span></span>
<span data-ttu-id="2eb05-133">Lokalizacja wystąpienia źródłowego zarządzanych kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="2eb05-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb05-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="2eb05-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="2eb05-135">Czy tylko uzyskać najnowszą kopię zapasową na bazę danych.</span><span class="sxs-lookup"><span data-stu-id="2eb05-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="2eb05-136">Wartość domyślna to FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="2eb05-136">Defaults to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb05-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb05-137">-ResourceGroupName</span></span>
<span data-ttu-id="2eb05-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2eb05-138">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb05-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb05-139">-ResourceId</span></span>
<span data-ttu-id="2eb05-140">Identyfikator zasobu bazy danych, dla którego mają zostać utworzone kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="2eb05-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb05-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2eb05-141">-Confirm</span></span>
<span data-ttu-id="2eb05-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eb05-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb05-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb05-143">-WhatIf</span></span>
<span data-ttu-id="2eb05-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eb05-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb05-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2eb05-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb05-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb05-146">CommonParameters</span></span>
<span data-ttu-id="2eb05-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb05-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb05-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eb05-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb05-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2eb05-149">INPUTS</span></span>

### <span data-ttu-id="2eb05-150">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2eb05-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="2eb05-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2eb05-151">System.String</span></span>

## <span data-ttu-id="2eb05-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2eb05-152">OUTPUTS</span></span>

### <span data-ttu-id="2eb05-153">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="2eb05-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="2eb05-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2eb05-154">NOTES</span></span>

## <span data-ttu-id="2eb05-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2eb05-155">RELATED LINKS</span></span>

[<span data-ttu-id="2eb05-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2eb05-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2eb05-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2eb05-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2eb05-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2eb05-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2eb05-159">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2eb05-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)