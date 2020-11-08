---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd57b5d6e4301b1ab22b041367388d37986a946e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053243"
---
# <span data-ttu-id="f8e8a-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="f8e8a-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="f8e8a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e8a-103">Zwraca informacje o bazie danych wystąpienia zarządzanego programu Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="f8e8a-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="f8e8a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8e8a-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8e8a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8e8a-105">DESCRIPTION</span></span>
<span data-ttu-id="f8e8a-106">Polecenie cmdlet **Get-AzSqlInstanceDatabaseGeoBackup umożliwia pobranie** co najmniej jednej bazy danych SQL platformy Azure, których kopie zapasowe są dublowane z wystąpienia zarządzanego bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e8a-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="f8e8a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8e8a-107">EXAMPLES</span></span>

### <span data-ttu-id="f8e8a-108">Przykład 1: pobieranie wszystkich rezerwowych kopii zapasowych baz danych w wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="f8e8a-108">Example 1: Get all database redundant backups on a instance</span></span>
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

<span data-ttu-id="f8e8a-109">To polecenie pobiera wszystkie nadmiarowe kopie zapasowe bazy danych z wystąpienia o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="f8e8a-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="f8e8a-110">Przykład 2: pobieranie bazy danych z nadmiarową kopią zapasową według nazwy w zarządzanym wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="f8e8a-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="f8e8a-111">To polecenie pobiera bazę danych o nadmiarowej kopii zapasowej o nazwie managedDatabase1 z wystąpienia o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="f8e8a-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="f8e8a-112">Przykład 3: pobieranie wszystkich zbędnych kopii zapasowych baz danych na instancji przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="f8e8a-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
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

<span data-ttu-id="f8e8a-113">To polecenie pobiera wszystkie nadmiarowe kopie zapasowe bazy danych z wystąpienia o nazwie managedInstance1, które rozpoczynają się od "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="f8e8a-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="f8e8a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8e8a-114">PARAMETERS</span></span>

### <span data-ttu-id="f8e8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e8a-115">-DefaultProfile</span></span>
<span data-ttu-id="f8e8a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e8a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8e8a-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f8e8a-117">-InstanceName</span></span>
<span data-ttu-id="f8e8a-118">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="f8e8a-118">The name of the instance.</span></span>

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

### <span data-ttu-id="f8e8a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8e8a-119">-Name</span></span>
<span data-ttu-id="f8e8a-120">Nazwa bazy danych wystąpienia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="f8e8a-120">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="f8e8a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e8a-121">-ResourceGroupName</span></span>
<span data-ttu-id="f8e8a-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8e8a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f8e8a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e8a-123">CommonParameters</span></span>
<span data-ttu-id="f8e8a-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8e8a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e8a-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8e8a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e8a-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8e8a-126">INPUTS</span></span>

### <span data-ttu-id="f8e8a-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f8e8a-127">None</span></span>

## <span data-ttu-id="f8e8a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8e8a-128">OUTPUTS</span></span>

### <span data-ttu-id="f8e8a-129">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f8e8a-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="f8e8a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8e8a-130">NOTES</span></span>

## <span data-ttu-id="f8e8a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8e8a-131">RELATED LINKS</span></span>
