---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: fe6779c64a3cbc5a484dd4a3ee3662bcdaf59059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544772"
---
# <span data-ttu-id="df803-101">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="df803-101">Get-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="df803-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df803-102">SYNOPSIS</span></span>
<span data-ttu-id="df803-103">Zwraca informacje o bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="df803-103">Returns information about Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df803-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df803-104">SYNTAX</span></span>

### <span data-ttu-id="df803-105">GetInstanceDatabaseFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df803-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df803-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="df803-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df803-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="df803-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df803-108">Opis</span><span class="sxs-lookup"><span data-stu-id="df803-108">DESCRIPTION</span></span>
<span data-ttu-id="df803-109">Polecenie cmdlet **Get-AzureRmSqlInstanceDatabase** pobiera co najmniej jeden program Azure SQL Database z wystąpienia zarządzanego bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="df803-109">The **Get-AzureRmSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="df803-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df803-110">EXAMPLES</span></span>

### <span data-ttu-id="df803-111">Przykład 1: pobieranie wszystkich baz danych w wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="df803-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
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

<span data-ttu-id="df803-112">To polecenie pobiera wszystkie bazy danych w wystąpieniu o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="df803-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="df803-113">Przykład 2: uzyskiwanie bazy danych według nazwy w zarządzanym wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="df803-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="df803-114">To polecenie pobiera bazę danych o nazwie managedDatabase1 z wystąpienia o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="df803-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

## <span data-ttu-id="df803-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df803-115">PARAMETERS</span></span>

### <span data-ttu-id="df803-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df803-116">-DefaultProfile</span></span>
<span data-ttu-id="df803-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df803-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df803-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="df803-118">-InstanceName</span></span>
<span data-ttu-id="df803-119">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="df803-119">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df803-120">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="df803-120">-InstanceObject</span></span>
<span data-ttu-id="df803-121">Obiekt wystąpienia, który ma zostać użyty do uzyskania bazy danych wystąpienia</span><span class="sxs-lookup"><span data-stu-id="df803-121">The instance object to use for getting instance database</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df803-122">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="df803-122">-InstanceResourceId</span></span>
<span data-ttu-id="df803-123">Identyfikator zasobu wystąpienia, który ma zostać wyświetlony</span><span class="sxs-lookup"><span data-stu-id="df803-123">The resource id of instance object to get</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df803-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df803-124">-Name</span></span>
<span data-ttu-id="df803-125">Nazwa bazy danych wystąpienia SQL Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="df803-125">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df803-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df803-126">-ResourceGroupName</span></span>
<span data-ttu-id="df803-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df803-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df803-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df803-128">CommonParameters</span></span>
<span data-ttu-id="df803-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df803-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df803-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df803-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df803-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df803-131">INPUTS</span></span>

### <span data-ttu-id="df803-132">System. String</span><span class="sxs-lookup"><span data-stu-id="df803-132">System.String</span></span>
<span data-ttu-id="df803-133">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="df803-133">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="df803-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df803-134">OUTPUTS</span></span>

### <span data-ttu-id="df803-135">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="df803-135">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="df803-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df803-136">NOTES</span></span>

## <span data-ttu-id="df803-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df803-137">RELATED LINKS</span></span>
