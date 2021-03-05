---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 88e08a15c864386d2e073f83f437d0db537f2ae7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003018"
---
# <span data-ttu-id="0675c-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="0675c-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="0675c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0675c-102">SYNOPSIS</span></span>
<span data-ttu-id="0675c-103">Ustawia typy informacji i etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="0675c-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="0675c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0675c-104">SYNTAX</span></span>

### <span data-ttu-id="0675c-105">ClassificationObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0675c-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0675c-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0675c-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0675c-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0675c-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0675c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0675c-108">DESCRIPTION</span></span>
<span data-ttu-id="0675c-109">Polecenie Set-AzSqlDatabaseSensitivityClassification ustawia typy informacji i etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="0675c-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="0675c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0675c-110">EXAMPLES</span></span>

### <span data-ttu-id="0675c-111">Przykład 1. Ustawianie typu informacji i etykiety wrażliwości kolumny w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0675c-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="0675c-112">Przykład 2. Ustawianie zalecanych typów informacji i etykiet wrażliwości kolumn w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0675c-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="0675c-113">Przykład 3. Ustawianie typu informacji i etykiety wrażliwości kolumny w bazie danych Azure SQL przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="0675c-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="0675c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0675c-114">PARAMETERS</span></span>

### <span data-ttu-id="0675c-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0675c-115">-AsJob</span></span>
<span data-ttu-id="0675c-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0675c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0675c-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="0675c-117">-ClassificationObject</span></span>
<span data-ttu-id="0675c-118">Obiekt reprezentujący klasyfikację wrażliwości bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="0675c-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="0675c-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0675c-119">-ColumnName</span></span>
<span data-ttu-id="0675c-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="0675c-120">Name of column.</span></span>

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

### <span data-ttu-id="0675c-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0675c-121">-DatabaseName</span></span>
<span data-ttu-id="0675c-122">Nazwa bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="0675c-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="0675c-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="0675c-123">-DatabaseObject</span></span>
<span data-ttu-id="0675c-124">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="0675c-124">The SQL database object.</span></span>

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

### <span data-ttu-id="0675c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0675c-125">-DefaultProfile</span></span>
<span data-ttu-id="0675c-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0675c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0675c-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="0675c-127">-InformationType</span></span>
<span data-ttu-id="0675c-128">Nazwa opisującą typ informacji przechowywanych w kolumnie.</span><span class="sxs-lookup"><span data-stu-id="0675c-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0675c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0675c-129">-PassThru</span></span>
<span data-ttu-id="0675c-130">Określa, czy model klasyfikacji wrażliwości ma być wyprowadzony na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0675c-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="0675c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0675c-131">-ResourceGroupName</span></span>
<span data-ttu-id="0675c-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0675c-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="0675c-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0675c-133">-SchemaName</span></span>
<span data-ttu-id="0675c-134">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="0675c-134">Name of schema.</span></span>

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

### <span data-ttu-id="0675c-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="0675c-135">-SensitivityLabel</span></span>
<span data-ttu-id="0675c-136">Nazwa opisującą charakter danych przechowywanych w kolumnie.</span><span class="sxs-lookup"><span data-stu-id="0675c-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0675c-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0675c-137">-ServerName</span></span>
<span data-ttu-id="0675c-138">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="0675c-138">SQL server name.</span></span>

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

### <span data-ttu-id="0675c-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="0675c-139">-TableName</span></span>
<span data-ttu-id="0675c-140">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="0675c-140">Name of table.</span></span>

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

### <span data-ttu-id="0675c-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0675c-141">-Confirm</span></span>
<span data-ttu-id="0675c-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0675c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0675c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0675c-143">-WhatIf</span></span>
<span data-ttu-id="0675c-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0675c-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0675c-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0675c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0675c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0675c-146">CommonParameters</span></span>
<span data-ttu-id="0675c-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0675c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0675c-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0675c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0675c-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0675c-149">INPUTS</span></span>

### <span data-ttu-id="0675c-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="0675c-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="0675c-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0675c-151">OUTPUTS</span></span>

### <span data-ttu-id="0675c-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0675c-152">System.Boolean</span></span>

## <span data-ttu-id="0675c-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0675c-153">NOTES</span></span>

## <span data-ttu-id="0675c-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0675c-154">RELATED LINKS</span></span>

[<span data-ttu-id="0675c-155">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="0675c-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
