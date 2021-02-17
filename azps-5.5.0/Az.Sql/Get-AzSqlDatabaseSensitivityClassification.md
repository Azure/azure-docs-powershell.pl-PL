---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: beada19e6b5ba7792c3fda6ca07ce987bd15fe2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191130"
---
# <span data-ttu-id="f4a82-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="f4a82-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="f4a82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4a82-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a82-103">Pobiera bieżące typy informacji i etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="f4a82-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="f4a82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f4a82-104">SYNTAX</span></span>

### <span data-ttu-id="f4a82-105">DatabaseObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f4a82-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4a82-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4a82-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4a82-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4a82-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4a82-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4a82-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4a82-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="f4a82-109">DESCRIPTION</span></span>
<span data-ttu-id="f4a82-110">Polecenie Get-AzSqlDatabaseSensitivityClassification zwraca bieżące typy informacji i etykiety wrażliwości kolumn w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f4a82-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="f4a82-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f4a82-111">EXAMPLES</span></span>

### <span data-ttu-id="f4a82-112">Przykład 1. Uzyskiwanie bieżących typów informacji i etykiet wrażliwości w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="f4a82-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
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

### <span data-ttu-id="f4a82-113">Przykład 2. Uzyskiwanie bieżących typów informacji i etykiet wrażliwości w usłudze Azure SQL Database za pomocą funkcji Piping.</span><span class="sxs-lookup"><span data-stu-id="f4a82-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
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

### <span data-ttu-id="f4a82-114">Przykład 3. Uzyskaj bieżący typ informacji i etykietę wrażliwości określonej kolumny w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="f4a82-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
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

### <span data-ttu-id="f4a82-115">Przykład 4. Pobierz bieżący typ informacji i etykietę wrażliwości określonej kolumny w usłudze Azure SQL Database za pomocą połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="f4a82-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
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

## <span data-ttu-id="f4a82-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4a82-116">PARAMETERS</span></span>

### <span data-ttu-id="f4a82-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f4a82-117">-AsJob</span></span>
<span data-ttu-id="f4a82-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f4a82-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4a82-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f4a82-119">-ColumnName</span></span>
<span data-ttu-id="f4a82-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="f4a82-120">Name of column.</span></span>

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

### <span data-ttu-id="f4a82-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4a82-121">-DatabaseName</span></span>
<span data-ttu-id="f4a82-122">Nazwa bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="f4a82-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="f4a82-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f4a82-123">-DatabaseObject</span></span>
<span data-ttu-id="f4a82-124">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f4a82-124">The SQL database object.</span></span>

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

### <span data-ttu-id="f4a82-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a82-125">-DefaultProfile</span></span>
<span data-ttu-id="f4a82-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a82-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4a82-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a82-127">-ResourceGroupName</span></span>
<span data-ttu-id="f4a82-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4a82-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4a82-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f4a82-129">-SchemaName</span></span>
<span data-ttu-id="f4a82-130">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="f4a82-130">Name of schema.</span></span>

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

### <span data-ttu-id="f4a82-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f4a82-131">-ServerName</span></span>
<span data-ttu-id="f4a82-132">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="f4a82-132">SQL server name.</span></span>

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

### <span data-ttu-id="f4a82-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="f4a82-133">-TableName</span></span>
<span data-ttu-id="f4a82-134">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="f4a82-134">Name of table.</span></span>

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

### <span data-ttu-id="f4a82-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a82-135">CommonParameters</span></span>
<span data-ttu-id="f4a82-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a82-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a82-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4a82-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a82-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4a82-138">INPUTS</span></span>

### <span data-ttu-id="f4a82-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f4a82-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f4a82-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4a82-140">OUTPUTS</span></span>

### <span data-ttu-id="f4a82-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="f4a82-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="f4a82-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f4a82-142">NOTES</span></span>

## <span data-ttu-id="f4a82-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4a82-143">RELATED LINKS</span></span>

[<span data-ttu-id="f4a82-144">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="f4a82-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
