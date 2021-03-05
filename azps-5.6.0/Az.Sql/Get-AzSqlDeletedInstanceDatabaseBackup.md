---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: 1d41e42b673eccc692c317f3e9d1d20c5551da4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999674"
---
# <span data-ttu-id="ed9bb-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="ed9bb-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="ed9bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed9bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9bb-103">Pobiera usuniętą bazę danych, która można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="ed9bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed9bb-104">SYNTAX</span></span>

### <span data-ttu-id="ed9bb-105">DeletedDatabaseList (Default)</span><span class="sxs-lookup"><span data-stu-id="ed9bb-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed9bb-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="ed9bb-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed9bb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed9bb-107">DESCRIPTION</span></span>
<span data-ttu-id="ed9bb-108">Polecenie **cmdlet Get-AzSqlDeletedInstanceDatabaseBackup** pobiera określoną usuniętą kopię zapasową bazy danych wystąpienia SQL, która można przywrócić, lub wszystkie usunięte kopie zapasowe, które można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="ed9bb-109">To polecenie cmdlet jest również obsługiwane przez usługę SQL Instance Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ed9bb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed9bb-110">EXAMPLES</span></span>

### <span data-ttu-id="ed9bb-111">Przykład 1. Uzyskiwanie wszystkich usuniętych kopii zapasowych bazy danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="ed9bb-111">Example 1: Get all deleted database backups on a server</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000

DeletionDate         : 2019-03-04 04:00:08 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB3
CreationDate         : 2019-03-04 03:00:31 AM
EarliestRestorePoint : 2019-03-04 03:05:23 AM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB3,13196145
                       6082100000
```

<span data-ttu-id="ed9bb-112">To polecenie pobiera wszystkie usunięte kopie zapasowe baz danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="ed9bb-113">Przykład 2. Uzyskiwanie określonej usuniętej kopii zapasowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="ed9bb-113">Example 2: Get a specified deleted database backup</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000
```

## <span data-ttu-id="ed9bb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed9bb-114">PARAMETERS</span></span>

### <span data-ttu-id="ed9bb-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed9bb-115">-DatabaseName</span></span>
<span data-ttu-id="ed9bb-116">Nazwa bazy danych Azure SQL Instance Database, dla których mają być pobierane kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9bb-117">-DefaultProfile</span></span>
<span data-ttu-id="ed9bb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed9bb-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="ed9bb-119">-DeletionDate</span></span>
<span data-ttu-id="ed9bb-120">Data usunięcia bazy danych Azure SQL Instance Database do pobierania kopii zapasowych z dokładnością milisekundy (np. 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="ed9bb-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bb-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ed9bb-121">-InstanceName</span></span>
<span data-ttu-id="ed9bb-122">Nazwa wystąpienia zarządzanego przez język Azure SQL, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed9bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed9bb-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9bb-125">CommonParameters</span></span>
<span data-ttu-id="ed9bb-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9bb-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed9bb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9bb-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed9bb-128">INPUTS</span></span>

### <span data-ttu-id="ed9bb-129">Brak</span><span class="sxs-lookup"><span data-stu-id="ed9bb-129">None</span></span>

## <span data-ttu-id="ed9bb-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed9bb-130">OUTPUTS</span></span>

### <span data-ttu-id="ed9bb-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="ed9bb-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="ed9bb-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed9bb-132">NOTES</span></span>

## <span data-ttu-id="ed9bb-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed9bb-133">RELATED LINKS</span></span>
