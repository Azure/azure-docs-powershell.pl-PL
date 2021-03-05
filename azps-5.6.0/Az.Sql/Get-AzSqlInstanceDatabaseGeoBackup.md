---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd66238627c96d2b3b1a8aaa2ebc7e2505515d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999466"
---
# <span data-ttu-id="42cf1-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="42cf1-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="42cf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="42cf1-103">Zwraca informacje o nadmiarowej kopii zapasowej bazy danych zarządzanej przez sql azure.</span><span class="sxs-lookup"><span data-stu-id="42cf1-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="42cf1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="42cf1-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42cf1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="42cf1-105">DESCRIPTION</span></span>
<span data-ttu-id="42cf1-106">Polecenie **cmdlet Get-AzSqlInstanceDatabaseGeoBackup** pobiera co najmniej jedną nadmiarową kopię zapasową baz danych Azure SQL z zarządzanego wystąpienia usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="42cf1-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="42cf1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="42cf1-107">EXAMPLES</span></span>

### <span data-ttu-id="42cf1-108">Przykład 1. Uzyskiwanie wszystkich nadmiarowych kopii zapasowych bazy danych w wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="42cf1-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="42cf1-109">To polecenie pobiera wszystkie nadmiarowe kopie zapasowe baz danych w wystąpieniu o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="42cf1-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="42cf1-110">Przykład 2. Uzyskiwanie nadmiarowej kopii zapasowej bazy danych według nazwy w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="42cf1-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="42cf1-111">To polecenie pobiera nadmiarowe kopie zapasowe bazy danych o nazwie managedDatabase1 z wystąpienia o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="42cf1-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="42cf1-112">Przykład 3. Uzyskiwanie wszystkich nadmiarowych kopii zapasowych bazy danych w wystąpieniu przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="42cf1-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="42cf1-113">To polecenie pobiera wszystkie nadmiarowe kopie zapasowe baz danych w wystąpieniu o nazwie managedInstance1, które zaczyna się od "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="42cf1-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="42cf1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42cf1-114">PARAMETERS</span></span>

### <span data-ttu-id="42cf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42cf1-115">-DefaultProfile</span></span>
<span data-ttu-id="42cf1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="42cf1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42cf1-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="42cf1-117">-InstanceName</span></span>
<span data-ttu-id="42cf1-118">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="42cf1-118">The name of the instance.</span></span>

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

### <span data-ttu-id="42cf1-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="42cf1-119">-Name</span></span>
<span data-ttu-id="42cf1-120">Nazwa wystąpienia bazy danych do pobrania.</span><span class="sxs-lookup"><span data-stu-id="42cf1-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cf1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42cf1-121">-ResourceGroupName</span></span>
<span data-ttu-id="42cf1-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42cf1-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cf1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42cf1-123">CommonParameters</span></span>
<span data-ttu-id="42cf1-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42cf1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42cf1-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42cf1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42cf1-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42cf1-126">INPUTS</span></span>

### <span data-ttu-id="42cf1-127">Brak</span><span class="sxs-lookup"><span data-stu-id="42cf1-127">None</span></span>

## <span data-ttu-id="42cf1-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42cf1-128">OUTPUTS</span></span>

### <span data-ttu-id="42cf1-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="42cf1-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="42cf1-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="42cf1-130">NOTES</span></span>

## <span data-ttu-id="42cf1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42cf1-131">RELATED LINKS</span></span>
