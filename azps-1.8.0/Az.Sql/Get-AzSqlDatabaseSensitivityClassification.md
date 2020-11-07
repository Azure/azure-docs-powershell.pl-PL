---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 50bd23f0c0be638683dae4acb5b43165a8c5b4f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707983"
---
# <span data-ttu-id="60419-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="60419-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="60419-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60419-102">SYNOPSIS</span></span>
<span data-ttu-id="60419-103">Pobiera bieżące typy informacji oraz etykiety liter kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="60419-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="60419-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60419-104">SYNTAX</span></span>

### <span data-ttu-id="60419-105">DatabaseObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="60419-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60419-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="60419-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60419-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="60419-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60419-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="60419-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60419-109">Opis</span><span class="sxs-lookup"><span data-stu-id="60419-109">DESCRIPTION</span></span>
<span data-ttu-id="60419-110">Polecenie cmdlet Get-AzSqlDatabaseSensitivityClassification zwraca bieżące typy informacji oraz etykiety liter kolumn w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="60419-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="60419-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60419-111">EXAMPLES</span></span>

### <span data-ttu-id="60419-112">Przykład 1: pobieranie bieżących typów informacji i etykiet liter w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="60419-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
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

### <span data-ttu-id="60419-113">Przykład 2: uzyskiwanie aktualnych typów informacji i etykiet wrażliwości bazy danych SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="60419-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
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

### <span data-ttu-id="60419-114">Przykład 3: uzyskiwanie aktualnego typu informacji i etykiety wrażliwości konkretnej kolumny bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="60419-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="60419-115">Przykład 4: uzyskiwanie informacji o typie i etykiecie wrażliwości konkretnej kolumny bazy danych SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="60419-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="60419-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60419-116">PARAMETERS</span></span>

### <span data-ttu-id="60419-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60419-117">-AsJob</span></span>
<span data-ttu-id="60419-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="60419-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60419-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="60419-119">-ColumnName</span></span>
<span data-ttu-id="60419-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="60419-120">Name of column.</span></span>

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

### <span data-ttu-id="60419-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="60419-121">-DatabaseName</span></span>
<span data-ttu-id="60419-122">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="60419-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="60419-123">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="60419-123">-DatabaseObject</span></span>
<span data-ttu-id="60419-124">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="60419-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60419-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60419-125">-DefaultProfile</span></span>
<span data-ttu-id="60419-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60419-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60419-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60419-127">-ResourceGroupName</span></span>
<span data-ttu-id="60419-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="60419-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="60419-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="60419-129">-SchemaName</span></span>
<span data-ttu-id="60419-130">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="60419-130">Name of schema.</span></span>

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

### <span data-ttu-id="60419-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="60419-131">-ServerName</span></span>
<span data-ttu-id="60419-132">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="60419-132">SQL server name.</span></span>

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

### <span data-ttu-id="60419-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="60419-133">-TableName</span></span>
<span data-ttu-id="60419-134">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="60419-134">Name of table.</span></span>

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

### <span data-ttu-id="60419-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60419-135">CommonParameters</span></span>
<span data-ttu-id="60419-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60419-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60419-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60419-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60419-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60419-138">INPUTS</span></span>

### <span data-ttu-id="60419-139">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="60419-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="60419-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60419-140">OUTPUTS</span></span>

### <span data-ttu-id="60419-141">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="60419-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="60419-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60419-142">NOTES</span></span>

## <span data-ttu-id="60419-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60419-143">RELATED LINKS</span></span>

[<span data-ttu-id="60419-144">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="60419-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
