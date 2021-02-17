---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177002"
---
# <span data-ttu-id="7605e-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="7605e-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="7605e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7605e-102">SYNOPSIS</span></span>
<span data-ttu-id="7605e-103">Włącza zalecenia wrażliwości dla kolumn (zalecenia są domyślnie włączone we wszystkich kolumnach) w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="7605e-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="7605e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7605e-104">SYNTAX</span></span>

### <span data-ttu-id="7605e-105">InputObjectParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7605e-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7605e-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7605e-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7605e-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7605e-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7605e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7605e-108">DESCRIPTION</span></span>
<span data-ttu-id="7605e-109">Polecenie Enable-AzSqlDatabaseSensitivityRecommendation umożliwia wyświetlanie rekomendacji wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="7605e-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="7605e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7605e-110">EXAMPLES</span></span>

### <span data-ttu-id="7605e-111">Przykład 1. Włączanie rekomendacji wrażliwości dla danej kolumny w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="7605e-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="7605e-112">Przykład 2. Włączanie rekomendacji wrażliwości dla danej kolumny w usłudze Azure SQL Database przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="7605e-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="7605e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7605e-113">PARAMETERS</span></span>

### <span data-ttu-id="7605e-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7605e-114">-AsJob</span></span>
<span data-ttu-id="7605e-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7605e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7605e-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7605e-116">-ColumnName</span></span>
<span data-ttu-id="7605e-117">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="7605e-117">Name of column.</span></span>

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

### <span data-ttu-id="7605e-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7605e-118">-DatabaseName</span></span>
<span data-ttu-id="7605e-119">Nazwa bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="7605e-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="7605e-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7605e-120">-DatabaseObject</span></span>
<span data-ttu-id="7605e-121">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="7605e-121">The SQL database object.</span></span>

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

### <span data-ttu-id="7605e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7605e-122">-DefaultProfile</span></span>
<span data-ttu-id="7605e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7605e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7605e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7605e-124">-InputObject</span></span>
<span data-ttu-id="7605e-125">Obiekt reprezentujący klasyfikację wrażliwości bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="7605e-125">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7605e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7605e-126">-PassThru</span></span>
<span data-ttu-id="7605e-127">Określa, czy model klasyfikacji wrażliwości ma być wyprowadzony na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7605e-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7605e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7605e-128">-ResourceGroupName</span></span>
<span data-ttu-id="7605e-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7605e-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="7605e-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7605e-130">-SchemaName</span></span>
<span data-ttu-id="7605e-131">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="7605e-131">Name of schema.</span></span>

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

### <span data-ttu-id="7605e-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7605e-132">-ServerName</span></span>
<span data-ttu-id="7605e-133">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="7605e-133">SQL server name.</span></span>

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

### <span data-ttu-id="7605e-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="7605e-134">-TableName</span></span>
<span data-ttu-id="7605e-135">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="7605e-135">Name of table.</span></span>

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

### <span data-ttu-id="7605e-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7605e-136">-Confirm</span></span>
<span data-ttu-id="7605e-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7605e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7605e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7605e-138">-WhatIf</span></span>
<span data-ttu-id="7605e-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7605e-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7605e-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7605e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7605e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7605e-141">CommonParameters</span></span>
<span data-ttu-id="7605e-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7605e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7605e-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7605e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7605e-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7605e-144">INPUTS</span></span>

### <span data-ttu-id="7605e-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7605e-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="7605e-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7605e-146">OUTPUTS</span></span>

### <span data-ttu-id="7605e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7605e-147">System.Boolean</span></span>

## <span data-ttu-id="7605e-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7605e-148">NOTES</span></span>

## <span data-ttu-id="7605e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7605e-149">RELATED LINKS</span></span>

[<span data-ttu-id="7605e-150">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="7605e-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)