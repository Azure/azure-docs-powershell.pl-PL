---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: bee6bd373c6b9c67afa8c70385c397d9334b733e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219801"
---
# <span data-ttu-id="b9306-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="b9306-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="b9306-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9306-102">SYNOPSIS</span></span>
<span data-ttu-id="b9306-103">Pobieranie usuniętej bazy danych, którą można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="b9306-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="b9306-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9306-104">SYNTAX</span></span>

### <span data-ttu-id="b9306-105">DeletedDatabaseList (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b9306-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9306-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="b9306-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9306-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b9306-107">DESCRIPTION</span></span>
<span data-ttu-id="b9306-108">Polecenie cmdlet **Get-AzSqlDeletedInstanceDatabaseBackup** pobiera określoną usuniętą kopię zapasową bazy danych wystąpienia SQL, którą można przywrócić, lub wszystkie usunięte kopie zapasowe, które można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="b9306-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="b9306-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server o ciągach na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b9306-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b9306-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9306-110">EXAMPLES</span></span>

### <span data-ttu-id="b9306-111">Przykład 1: pobieranie wszystkich usuniętych kopii zapasowych baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="b9306-111">Example 1: Get all deleted database backups on a server</span></span>
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

<span data-ttu-id="b9306-112">To polecenie pobiera wszystkie kopie zapasowe usunięte z bazy danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="b9306-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="b9306-113">Przykład 2: pobieranie określonej usuniętej kopii zapasowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="b9306-113">Example 2: Get a specified deleted database backup</span></span>
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

## <span data-ttu-id="b9306-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9306-114">PARAMETERS</span></span>

### <span data-ttu-id="b9306-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b9306-115">-DatabaseName</span></span>
<span data-ttu-id="b9306-116">Nazwa bazy danych wystąpienia SQL Azure, do której mają być pobierane kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="b9306-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="b9306-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9306-117">-DefaultProfile</span></span>
<span data-ttu-id="b9306-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9306-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9306-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="b9306-119">-DeletionDate</span></span>
<span data-ttu-id="b9306-120">Data usunięcia bazy danych wystąpienia SQL Azure w celu pobrania kopii zapasowych z dokładnością do milisekund (na przykład 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="b9306-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="b9306-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b9306-121">-InstanceName</span></span>
<span data-ttu-id="b9306-122">Nazwa wystąpienia zarządzanego w usłudze Azure SQL, w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="b9306-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="b9306-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9306-123">-ResourceGroupName</span></span>
<span data-ttu-id="b9306-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b9306-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9306-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9306-125">CommonParameters</span></span>
<span data-ttu-id="b9306-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9306-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9306-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9306-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9306-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9306-128">INPUTS</span></span>

### <span data-ttu-id="b9306-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b9306-129">None</span></span>

## <span data-ttu-id="b9306-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9306-130">OUTPUTS</span></span>

### <span data-ttu-id="b9306-131">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. model. AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="b9306-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="b9306-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9306-132">NOTES</span></span>

## <span data-ttu-id="b9306-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9306-133">RELATED LINKS</span></span>
