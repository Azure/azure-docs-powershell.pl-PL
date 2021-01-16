---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 15da7969c5e47376e04bb78a02ff611c9326b947
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341941"
---
# <span data-ttu-id="675cc-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="675cc-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="675cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="675cc-102">SYNOPSIS</span></span>
<span data-ttu-id="675cc-103">Usuwa typy informacji oraz etykiety liter kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="675cc-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="675cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="675cc-104">SYNTAX</span></span>

### <span data-ttu-id="675cc-105">ClassificationObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="675cc-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="675cc-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="675cc-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="675cc-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="675cc-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="675cc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="675cc-108">DESCRIPTION</span></span>
<span data-ttu-id="675cc-109">Polecenie cmdlet Remove-AzSqlDatabaseSensitivityClassification usuwa typy informacji oraz etykiety liter kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="675cc-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="675cc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="675cc-110">EXAMPLES</span></span>

### <span data-ttu-id="675cc-111">Przykład 1: usuwanie typu informacji i etykiety wrażliwości kolumny w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="675cc-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="675cc-112">Przykład 2: usuwanie bieżących typów informacji i etykiet liter kolumn w bazie danych SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="675cc-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="675cc-113">Przykład 3: usuwanie typu informacji i etykiety wrażliwości kolumny w bazie danych SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="675cc-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="675cc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="675cc-114">PARAMETERS</span></span>

### <span data-ttu-id="675cc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="675cc-115">-AsJob</span></span>
<span data-ttu-id="675cc-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="675cc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="675cc-117">-Klasyfikacyjnobject</span><span class="sxs-lookup"><span data-stu-id="675cc-117">-ClassificationObject</span></span>
<span data-ttu-id="675cc-118">Obiekt reprezentujący klasyfikację wrażliwości bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="675cc-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="675cc-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="675cc-119">-ColumnName</span></span>
<span data-ttu-id="675cc-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="675cc-120">Name of column.</span></span>

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

### <span data-ttu-id="675cc-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="675cc-121">-DatabaseName</span></span>
<span data-ttu-id="675cc-122">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="675cc-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="675cc-123">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="675cc-123">-DatabaseObject</span></span>
<span data-ttu-id="675cc-124">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="675cc-124">The SQL database object.</span></span>

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

### <span data-ttu-id="675cc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="675cc-125">-DefaultProfile</span></span>
<span data-ttu-id="675cc-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="675cc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="675cc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="675cc-127">-PassThru</span></span>
<span data-ttu-id="675cc-128">Określa, czy ma być wyprowadzany model klasyfikacji wrażliwości na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="675cc-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="675cc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="675cc-129">-ResourceGroupName</span></span>
<span data-ttu-id="675cc-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="675cc-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="675cc-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="675cc-131">-SchemaName</span></span>
<span data-ttu-id="675cc-132">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="675cc-132">Name of schema.</span></span>

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

### <span data-ttu-id="675cc-133">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="675cc-133">-ServerName</span></span>
<span data-ttu-id="675cc-134">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="675cc-134">SQL server name.</span></span>

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

### <span data-ttu-id="675cc-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="675cc-135">-TableName</span></span>
<span data-ttu-id="675cc-136">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="675cc-136">Name of table.</span></span>

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

### <span data-ttu-id="675cc-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="675cc-137">-Confirm</span></span>
<span data-ttu-id="675cc-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="675cc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="675cc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="675cc-139">-WhatIf</span></span>
<span data-ttu-id="675cc-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="675cc-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="675cc-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="675cc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="675cc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="675cc-142">CommonParameters</span></span>
<span data-ttu-id="675cc-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="675cc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="675cc-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="675cc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="675cc-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="675cc-145">INPUTS</span></span>

### <span data-ttu-id="675cc-146">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="675cc-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="675cc-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="675cc-147">OUTPUTS</span></span>

### <span data-ttu-id="675cc-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="675cc-148">System.Boolean</span></span>

## <span data-ttu-id="675cc-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="675cc-149">NOTES</span></span>

## <span data-ttu-id="675cc-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="675cc-150">RELATED LINKS</span></span>

[<span data-ttu-id="675cc-151">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="675cc-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
