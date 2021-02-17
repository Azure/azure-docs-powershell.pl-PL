---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 15da7969c5e47376e04bb78a02ff611c9326b947
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176842"
---
# <span data-ttu-id="9d3b4-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="9d3b4-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="9d3b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="9d3b4-103">Usuwa typy informacji i etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="9d3b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d3b4-104">SYNTAX</span></span>

### <span data-ttu-id="9d3b4-105">ClassificationObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9d3b4-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d3b4-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d3b4-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d3b4-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d3b4-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d3b4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d3b4-108">DESCRIPTION</span></span>
<span data-ttu-id="9d3b4-109">Polecenie Remove-AzSqlDatabaseSensitivityClassification cmdlet usuwa typy informacji i etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="9d3b4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d3b4-110">EXAMPLES</span></span>

### <span data-ttu-id="9d3b4-111">Przykład 1. Usuwanie typu informacji i etykiety wrażliwości kolumny w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="9d3b4-112">Przykład 2. Usuwanie bieżących typów informacji i etykiet wrażliwości kolumn w bazie danych Azure SQL przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="9d3b4-113">Przykład 3. Usuwanie typu informacji i etykiety wrażliwości kolumny w bazie danych Azure SQL przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="9d3b4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d3b4-114">PARAMETERS</span></span>

### <span data-ttu-id="9d3b4-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9d3b4-115">-AsJob</span></span>
<span data-ttu-id="9d3b4-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9d3b4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d3b4-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="9d3b4-117">-ClassificationObject</span></span>
<span data-ttu-id="9d3b4-118">Obiekt reprezentujący klasyfikację wrażliwości bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9d3b4-119">-ColumnName</span></span>
<span data-ttu-id="9d3b4-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-120">Name of column.</span></span>

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

### <span data-ttu-id="9d3b4-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9d3b4-121">-DatabaseName</span></span>
<span data-ttu-id="9d3b4-122">Nazwa bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9d3b4-123">-DatabaseObject</span></span>
<span data-ttu-id="9d3b4-124">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d3b4-125">-DefaultProfile</span></span>
<span data-ttu-id="9d3b4-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d3b4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d3b4-127">-PassThru</span></span>
<span data-ttu-id="9d3b4-128">Określa, czy model klasyfikacji wrażliwości ma być wyprowadzony na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9d3b4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d3b4-129">-ResourceGroupName</span></span>
<span data-ttu-id="9d3b4-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9d3b4-131">-SchemaName</span></span>
<span data-ttu-id="9d3b4-132">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-132">Name of schema.</span></span>

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

### <span data-ttu-id="9d3b4-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9d3b4-133">-ServerName</span></span>
<span data-ttu-id="9d3b4-134">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-134">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="9d3b4-135">-TableName</span></span>
<span data-ttu-id="9d3b4-136">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-136">Name of table.</span></span>

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

### <span data-ttu-id="9d3b4-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d3b4-137">-Confirm</span></span>
<span data-ttu-id="9d3b4-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d3b4-139">-WhatIf</span></span>
<span data-ttu-id="9d3b4-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d3b4-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d3b4-142">CommonParameters</span></span>
<span data-ttu-id="9d3b4-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d3b4-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d3b4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d3b4-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d3b4-145">INPUTS</span></span>

### <span data-ttu-id="9d3b4-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9d3b4-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9d3b4-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d3b4-147">OUTPUTS</span></span>

### <span data-ttu-id="9d3b4-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9d3b4-148">System.Boolean</span></span>

## <span data-ttu-id="9d3b4-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d3b4-149">NOTES</span></span>

## <span data-ttu-id="9d3b4-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d3b4-150">RELATED LINKS</span></span>

[<span data-ttu-id="9d3b4-151">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="9d3b4-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
