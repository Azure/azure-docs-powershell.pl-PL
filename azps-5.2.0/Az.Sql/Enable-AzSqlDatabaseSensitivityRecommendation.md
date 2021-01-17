---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327936"
---
# <span data-ttu-id="34daa-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="34daa-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="34daa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34daa-102">SYNOPSIS</span></span>
<span data-ttu-id="34daa-103">Włącza rekomendacje dotyczące wrażliwości na kolumny (rekomendacje są domyślnie włączone we wszystkich kolumnach) w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="34daa-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="34daa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34daa-104">SYNTAX</span></span>

### <span data-ttu-id="34daa-105">InputObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34daa-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34daa-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="34daa-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34daa-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="34daa-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34daa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="34daa-108">DESCRIPTION</span></span>
<span data-ttu-id="34daa-109">Polecenie cmdlet Enable-AzSqlDatabaseSensitivityRecommendation włącza zalecenia dotyczące wrażliwości na kolumny w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="34daa-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="34daa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34daa-110">EXAMPLES</span></span>

### <span data-ttu-id="34daa-111">Przykład 1: Włączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="34daa-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="34daa-112">Przykład 2: Włączanie rekomendacji dotyczących wrażliwości dla danej kolumny bazy danych Azure SQL Database przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="34daa-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="34daa-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34daa-113">PARAMETERS</span></span>

### <span data-ttu-id="34daa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34daa-114">-AsJob</span></span>
<span data-ttu-id="34daa-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="34daa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34daa-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="34daa-116">-ColumnName</span></span>
<span data-ttu-id="34daa-117">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="34daa-117">Name of column.</span></span>

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

### <span data-ttu-id="34daa-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34daa-118">-DatabaseName</span></span>
<span data-ttu-id="34daa-119">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="34daa-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="34daa-120">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="34daa-120">-DatabaseObject</span></span>
<span data-ttu-id="34daa-121">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="34daa-121">The SQL database object.</span></span>

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

### <span data-ttu-id="34daa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34daa-122">-DefaultProfile</span></span>
<span data-ttu-id="34daa-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34daa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34daa-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34daa-124">-InputObject</span></span>
<span data-ttu-id="34daa-125">Obiekt reprezentujący klasyfikację wrażliwości bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="34daa-125">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="34daa-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34daa-126">-PassThru</span></span>
<span data-ttu-id="34daa-127">Określa, czy ma być wyprowadzany model klasyfikacji wrażliwości na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34daa-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="34daa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34daa-128">-ResourceGroupName</span></span>
<span data-ttu-id="34daa-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34daa-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="34daa-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="34daa-130">-SchemaName</span></span>
<span data-ttu-id="34daa-131">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="34daa-131">Name of schema.</span></span>

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

### <span data-ttu-id="34daa-132">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="34daa-132">-ServerName</span></span>
<span data-ttu-id="34daa-133">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="34daa-133">SQL server name.</span></span>

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

### <span data-ttu-id="34daa-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="34daa-134">-TableName</span></span>
<span data-ttu-id="34daa-135">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="34daa-135">Name of table.</span></span>

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

### <span data-ttu-id="34daa-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34daa-136">-Confirm</span></span>
<span data-ttu-id="34daa-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34daa-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34daa-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34daa-138">-WhatIf</span></span>
<span data-ttu-id="34daa-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34daa-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34daa-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34daa-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34daa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34daa-141">CommonParameters</span></span>
<span data-ttu-id="34daa-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34daa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34daa-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34daa-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34daa-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34daa-144">INPUTS</span></span>

### <span data-ttu-id="34daa-145">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="34daa-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="34daa-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34daa-146">OUTPUTS</span></span>

### <span data-ttu-id="34daa-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34daa-147">System.Boolean</span></span>

## <span data-ttu-id="34daa-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34daa-148">NOTES</span></span>

## <span data-ttu-id="34daa-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34daa-149">RELATED LINKS</span></span>

[<span data-ttu-id="34daa-150">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="34daa-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)