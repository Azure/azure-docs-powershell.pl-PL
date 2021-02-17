---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188091"
---
# <span data-ttu-id="baf23-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="baf23-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="baf23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baf23-102">SYNOPSIS</span></span>
<span data-ttu-id="baf23-103">Zwraca informacje o bazie danych azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="baf23-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="baf23-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="baf23-104">SYNTAX</span></span>

### <span data-ttu-id="baf23-105">GetInstanceDatabaseFromInputParameters (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="baf23-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baf23-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="baf23-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baf23-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="baf23-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baf23-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="baf23-108">DESCRIPTION</span></span>
<span data-ttu-id="baf23-109">Polecenie **cmdlet Get-AzSqlInstanceDatabase** pobiera jedną lub więcej baz danych Azure SQL z zarządzanego wystąpienia usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="baf23-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="baf23-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="baf23-110">EXAMPLES</span></span>

### <span data-ttu-id="baf23-111">Przykład 1. Uzyskiwanie wszystkich baz danych w wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="baf23-111">Example 1: Get all databases on a instance</span></span>
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

<span data-ttu-id="baf23-112">To polecenie pobiera wszystkie bazy danych w wystąpieniu o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="baf23-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="baf23-113">Przykład 2. Uzyskiwanie bazy danych według nazwy w wystąpieniu zarządzanym</span><span class="sxs-lookup"><span data-stu-id="baf23-113">Example 2: Get a database by name on a Managed instance</span></span>
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

<span data-ttu-id="baf23-114">To polecenie pobiera bazę danych o nazwie managedDatabase1 z wystąpienia o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="baf23-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="baf23-115">Przykład 3. Uzyskiwanie wszystkich baz danych w wystąpieniu przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="baf23-115">Example 3: Get all databases on a instance using filtering</span></span>
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

<span data-ttu-id="baf23-116">To polecenie pobiera wszystkie bazy danych w wystąpieniu o nazwie managedInstance1, które zaczynają się od "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="baf23-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="baf23-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baf23-117">PARAMETERS</span></span>

### <span data-ttu-id="baf23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf23-118">-DefaultProfile</span></span>
<span data-ttu-id="baf23-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="baf23-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baf23-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="baf23-120">-InstanceName</span></span>
<span data-ttu-id="baf23-121">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="baf23-121">The instance name.</span></span>

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

### <span data-ttu-id="baf23-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="baf23-122">-InstanceObject</span></span>
<span data-ttu-id="baf23-123">Obiekt wystąpienia do użycia w celu uzyskania bazy danych wystąpienia</span><span class="sxs-lookup"><span data-stu-id="baf23-123">The instance object to use for getting instance database</span></span>

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

### <span data-ttu-id="baf23-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="baf23-124">-InstanceResourceId</span></span>
<span data-ttu-id="baf23-125">Identyfikator zasobu obiektu wystąpienia do uzyskania</span><span class="sxs-lookup"><span data-stu-id="baf23-125">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="baf23-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="baf23-126">-Name</span></span>
<span data-ttu-id="baf23-127">Nazwa bazy danych Azure SQL Instance Database do pobrania.</span><span class="sxs-lookup"><span data-stu-id="baf23-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf23-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf23-128">-ResourceGroupName</span></span>
<span data-ttu-id="baf23-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="baf23-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="baf23-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf23-130">CommonParameters</span></span>
<span data-ttu-id="baf23-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf23-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf23-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="baf23-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf23-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baf23-133">INPUTS</span></span>

### <span data-ttu-id="baf23-134">System.String</span><span class="sxs-lookup"><span data-stu-id="baf23-134">System.String</span></span>

### <span data-ttu-id="baf23-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="baf23-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="baf23-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baf23-136">OUTPUTS</span></span>

### <span data-ttu-id="baf23-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="baf23-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="baf23-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="baf23-138">NOTES</span></span>

## <span data-ttu-id="baf23-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="baf23-139">RELATED LINKS</span></span>
