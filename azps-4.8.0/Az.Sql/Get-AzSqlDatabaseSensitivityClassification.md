---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: beada19e6b5ba7792c3fda6ca07ce987bd15fe2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063165"
---
# <span data-ttu-id="55f21-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="55f21-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="55f21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55f21-102">SYNOPSIS</span></span>
<span data-ttu-id="55f21-103">Pobiera bieżące typy informacji oraz etykiety liter kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="55f21-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="55f21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55f21-104">SYNTAX</span></span>

### <span data-ttu-id="55f21-105">DatabaseObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="55f21-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55f21-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f21-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55f21-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f21-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55f21-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f21-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55f21-109">Opis</span><span class="sxs-lookup"><span data-stu-id="55f21-109">DESCRIPTION</span></span>
<span data-ttu-id="55f21-110">Polecenie cmdlet Get-AzSqlDatabaseSensitivityClassification zwraca bieżące typy informacji oraz etykiety liter kolumn w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="55f21-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="55f21-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55f21-111">EXAMPLES</span></span>

### <span data-ttu-id="55f21-112">Przykład 1: pobieranie bieżących typów informacji i etykiet liter w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="55f21-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="55f21-113">Przykład 2: uzyskiwanie aktualnych typów informacji i etykiet wrażliwości bazy danych SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="55f21-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="55f21-114">Przykład 3: uzyskiwanie aktualnego typu informacji i etykiety wrażliwości konkretnej kolumny bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="55f21-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="55f21-115">Przykład 4: uzyskiwanie informacji o typie i etykiecie wrażliwości konkretnej kolumny bazy danych SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="55f21-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="55f21-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55f21-116">PARAMETERS</span></span>

### <span data-ttu-id="55f21-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55f21-117">-AsJob</span></span>
<span data-ttu-id="55f21-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="55f21-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55f21-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="55f21-119">-ColumnName</span></span>
<span data-ttu-id="55f21-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="55f21-120">Name of column.</span></span>

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

### <span data-ttu-id="55f21-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="55f21-121">-DatabaseName</span></span>
<span data-ttu-id="55f21-122">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="55f21-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="55f21-123">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="55f21-123">-DatabaseObject</span></span>
<span data-ttu-id="55f21-124">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="55f21-124">The SQL database object.</span></span>

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

### <span data-ttu-id="55f21-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f21-125">-DefaultProfile</span></span>
<span data-ttu-id="55f21-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55f21-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55f21-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f21-127">-ResourceGroupName</span></span>
<span data-ttu-id="55f21-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55f21-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="55f21-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="55f21-129">-SchemaName</span></span>
<span data-ttu-id="55f21-130">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="55f21-130">Name of schema.</span></span>

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

### <span data-ttu-id="55f21-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="55f21-131">-ServerName</span></span>
<span data-ttu-id="55f21-132">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="55f21-132">SQL server name.</span></span>

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

### <span data-ttu-id="55f21-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="55f21-133">-TableName</span></span>
<span data-ttu-id="55f21-134">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="55f21-134">Name of table.</span></span>

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

### <span data-ttu-id="55f21-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f21-135">CommonParameters</span></span>
<span data-ttu-id="55f21-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55f21-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f21-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55f21-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f21-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55f21-138">INPUTS</span></span>

### <span data-ttu-id="55f21-139">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="55f21-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="55f21-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55f21-140">OUTPUTS</span></span>

### <span data-ttu-id="55f21-141">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="55f21-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="55f21-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55f21-142">NOTES</span></span>

## <span data-ttu-id="55f21-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55f21-143">RELATED LINKS</span></span>

[<span data-ttu-id="55f21-144">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="55f21-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
