---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 89190f171ec9634e13eaa56499f6eca87e75ccf5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886934"
---
# <span data-ttu-id="b7424-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="b7424-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="b7424-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7424-102">SYNOPSIS</span></span>
<span data-ttu-id="b7424-103">Pobiera bieżące typy informacji oraz etykiety liter kolumn w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b7424-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b7424-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7424-104">SYNTAX</span></span>

### <span data-ttu-id="b7424-105">DatabaseObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7424-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7424-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7424-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7424-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7424-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7424-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7424-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7424-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b7424-109">DESCRIPTION</span></span>
<span data-ttu-id="b7424-110">Polecenie cmdlet Get-AzSqlInstanceDatabaseSensitivityClassification zwraca bieżące typy informacji oraz etykiety liter kolumn w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b7424-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b7424-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7424-111">EXAMPLES</span></span>

### <span data-ttu-id="b7424-112">Przykład 1: pobieranie bieżących typów informacji i etykiet liter w bazie danych wystąpień zarządzanych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b7424-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="b7424-113">Przykład 2: Uzyskaj aktualne typy informacji i etykiet wrażliwości bazy danych wystąpienia zarządzanego SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="b7424-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="b7424-114">Przykład 3: uzyskiwanie aktualnego typu informacji i etykiety czułości określonej kolumny bazy danych wystąpienia zarządzanego w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b7424-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="b7424-115">Przykład 4: uzyskiwanie informacji o typie i etykiecie wrażliwości konkretnej kolumny bazy danych wystąpienia zarządzanego SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="b7424-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="b7424-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7424-116">PARAMETERS</span></span>

### <span data-ttu-id="b7424-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7424-117">-AsJob</span></span>
<span data-ttu-id="b7424-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b7424-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7424-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b7424-119">-ColumnName</span></span>
<span data-ttu-id="b7424-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="b7424-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7424-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7424-121">-DatabaseName</span></span>
<span data-ttu-id="b7424-122">Nazwa bazy danych wystąpienia zarządzanego w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b7424-122">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7424-123">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="b7424-123">-DatabaseObject</span></span>
<span data-ttu-id="b7424-124">Obiekt bazy danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b7424-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7424-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7424-125">-DefaultProfile</span></span>
<span data-ttu-id="b7424-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7424-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7424-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b7424-127">-InstanceName</span></span>
<span data-ttu-id="b7424-128">Nazwa wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b7424-128">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7424-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7424-129">-ResourceGroupName</span></span>
<span data-ttu-id="b7424-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7424-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7424-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b7424-131">-SchemaName</span></span>
<span data-ttu-id="b7424-132">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="b7424-132">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7424-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="b7424-133">-TableName</span></span>
<span data-ttu-id="b7424-134">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="b7424-134">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7424-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7424-135">CommonParameters</span></span>
<span data-ttu-id="b7424-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7424-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7424-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7424-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7424-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7424-138">INPUTS</span></span>

### <span data-ttu-id="b7424-139">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b7424-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="b7424-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7424-140">OUTPUTS</span></span>

### <span data-ttu-id="b7424-141">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b7424-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="b7424-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7424-142">NOTES</span></span>

## <span data-ttu-id="b7424-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7424-143">RELATED LINKS</span></span>

[<span data-ttu-id="b7424-144">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b7424-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
