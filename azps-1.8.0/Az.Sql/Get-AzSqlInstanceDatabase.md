---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 63eb337f4c81658b8263066dd39e1af0634c49e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707942"
---
# <span data-ttu-id="737ff-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="737ff-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="737ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="737ff-102">SYNOPSIS</span></span>
<span data-ttu-id="737ff-103">Zwraca informacje o bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="737ff-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="737ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="737ff-104">SYNTAX</span></span>

### <span data-ttu-id="737ff-105">GetInstanceDatabaseFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="737ff-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="737ff-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="737ff-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="737ff-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="737ff-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="737ff-108">Opis</span><span class="sxs-lookup"><span data-stu-id="737ff-108">DESCRIPTION</span></span>
<span data-ttu-id="737ff-109">Polecenie cmdlet **Get-AzSqlInstanceDatabase** pobiera co najmniej jeden program Azure SQL Database z wystąpienia zarządzanego bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="737ff-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="737ff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="737ff-110">EXAMPLES</span></span>

### <span data-ttu-id="737ff-111">Przykład 1: pobieranie wszystkich baz danych w wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="737ff-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="737ff-112">To polecenie pobiera wszystkie bazy danych w wystąpieniu o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="737ff-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="737ff-113">Przykład 2: uzyskiwanie bazy danych według nazwy w zarządzanym wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="737ff-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="737ff-114">To polecenie pobiera bazę danych o nazwie managedDatabase1 z wystąpienia o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="737ff-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="737ff-115">Przykład 3: pobieranie wszystkich baz danych w wystąpieniu przy użyciu funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="737ff-115">Example 3: Get all databases on a instance using filtering</span></span>
```
PS C:\> Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="737ff-116">To polecenie pobiera wszystkie bazy danych w wystąpieniu o nazwie managedInstance1, które zaczynają się od "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="737ff-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="737ff-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="737ff-117">PARAMETERS</span></span>

### <span data-ttu-id="737ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737ff-118">-DefaultProfile</span></span>
<span data-ttu-id="737ff-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="737ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737ff-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="737ff-120">-InstanceName</span></span>
<span data-ttu-id="737ff-121">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="737ff-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737ff-122">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="737ff-122">-InstanceObject</span></span>
<span data-ttu-id="737ff-123">Obiekt wystąpienia, który ma zostać użyty do uzyskania bazy danych wystąpienia</span><span class="sxs-lookup"><span data-stu-id="737ff-123">The instance object to use for getting instance database</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="737ff-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="737ff-124">-InstanceResourceId</span></span>
<span data-ttu-id="737ff-125">Identyfikator zasobu wystąpienia, który ma zostać wyświetlony</span><span class="sxs-lookup"><span data-stu-id="737ff-125">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737ff-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="737ff-126">-Name</span></span>
<span data-ttu-id="737ff-127">Nazwa bazy danych wystąpienia SQL Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="737ff-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="737ff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737ff-128">-ResourceGroupName</span></span>
<span data-ttu-id="737ff-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="737ff-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737ff-130">CommonParameters</span></span>
<span data-ttu-id="737ff-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737ff-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="737ff-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737ff-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="737ff-133">INPUTS</span></span>

### <span data-ttu-id="737ff-134">System. String</span><span class="sxs-lookup"><span data-stu-id="737ff-134">System.String</span></span>

### <span data-ttu-id="737ff-135">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="737ff-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="737ff-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="737ff-136">OUTPUTS</span></span>

### <span data-ttu-id="737ff-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="737ff-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="737ff-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="737ff-138">NOTES</span></span>

## <span data-ttu-id="737ff-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="737ff-139">RELATED LINKS</span></span>