---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: bee6bd373c6b9c67afa8c70385c397d9334b733e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197722"
---
# <span data-ttu-id="5c7e0-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="5c7e0-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="5c7e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7e0-103">Pobiera usuniętą bazę danych, która można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="5c7e0-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="5c7e0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5c7e0-104">SYNTAX</span></span>

### <span data-ttu-id="5c7e0-105">DeletedDatabaseList (Default)</span><span class="sxs-lookup"><span data-stu-id="5c7e0-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c7e0-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="5c7e0-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c7e0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5c7e0-107">DESCRIPTION</span></span>
<span data-ttu-id="5c7e0-108">Polecenie **cmdlet Get-AzSqlDeletedInstanceDatabaseBackup** pobiera określoną usuniętą kopię zapasową bazy danych wystąpienia SQL, która można przywrócić, lub wszystkie usunięte kopie zapasowe, które można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="5c7e0-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="5c7e0-109">To polecenie cmdlet jest również obsługiwane przez usługę SQL Instance Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5c7e0-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5c7e0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5c7e0-110">EXAMPLES</span></span>

### <span data-ttu-id="5c7e0-111">Przykład 1. Uzyskiwanie wszystkich usuniętych kopii zapasowych bazy danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="5c7e0-111">Example 1: Get all deleted database backups on a server</span></span>
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

<span data-ttu-id="5c7e0-112">To polecenie pobiera wszystkie usunięte kopie zapasowe baz danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="5c7e0-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="5c7e0-113">Przykład 2. Uzyskiwanie określonej usuniętej kopii zapasowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="5c7e0-113">Example 2: Get a specified deleted database backup</span></span>
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

## <span data-ttu-id="5c7e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c7e0-114">PARAMETERS</span></span>

### <span data-ttu-id="5c7e0-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c7e0-115">-DatabaseName</span></span>
<span data-ttu-id="5c7e0-116">Nazwa bazy danych Azure SQL Instance Database, dla których mają być pobierane kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="5c7e0-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="5c7e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7e0-117">-DefaultProfile</span></span>
<span data-ttu-id="5c7e0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c7e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c7e0-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="5c7e0-119">-DeletionDate</span></span>
<span data-ttu-id="5c7e0-120">Data usunięcia bazy danych Azure SQL Instance Database do pobierania kopii zapasowych z dokładnością milisekundy (np. 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="5c7e0-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="5c7e0-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5c7e0-121">-InstanceName</span></span>
<span data-ttu-id="5c7e0-122">Nazwa wystąpienia zarządzanego przez usługę Azure SQL, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="5c7e0-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="5c7e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c7e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="5c7e0-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c7e0-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5c7e0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7e0-125">CommonParameters</span></span>
<span data-ttu-id="5c7e0-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c7e0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7e0-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c7e0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7e0-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c7e0-128">INPUTS</span></span>

### <span data-ttu-id="5c7e0-129">Brak</span><span class="sxs-lookup"><span data-stu-id="5c7e0-129">None</span></span>

## <span data-ttu-id="5c7e0-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c7e0-130">OUTPUTS</span></span>

### <span data-ttu-id="5c7e0-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="5c7e0-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="5c7e0-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5c7e0-132">NOTES</span></span>

## <span data-ttu-id="5c7e0-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c7e0-133">RELATED LINKS</span></span>
