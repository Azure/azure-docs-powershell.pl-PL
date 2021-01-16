---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368641"
---
# <span data-ttu-id="c8263-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="c8263-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="c8263-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8263-102">SYNOPSIS</span></span>
<span data-ttu-id="c8263-103">Wyłączenie (odrzucanie) rekomendacji dotyczących wrażliwości na kolumny w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="c8263-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="c8263-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8263-104">SYNTAX</span></span>

### <span data-ttu-id="c8263-105">InputObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c8263-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8263-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8263-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8263-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8263-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8263-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c8263-108">DESCRIPTION</span></span>
<span data-ttu-id="c8263-109">Polecenie cmdlet Disable-AzSqlDatabaseSensitivityRecommendation wyłącza (odrzuca) zalecenia dotyczące wrażliwości na kolumny w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="c8263-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="c8263-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8263-110">EXAMPLES</span></span>

### <span data-ttu-id="c8263-111">Przykład 1: wyłączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c8263-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="c8263-112">Przykład 2: wyłączanie zaleceń dotyczących wrażliwości na kolumny, które mają rekomendacje dotyczące wrażliwości w bazie danych SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="c8263-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="c8263-113">Przykład 3: wyłączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="c8263-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="c8263-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8263-114">PARAMETERS</span></span>

### <span data-ttu-id="c8263-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8263-115">-AsJob</span></span>
<span data-ttu-id="c8263-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c8263-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8263-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="c8263-117">-ColumnName</span></span>
<span data-ttu-id="c8263-118">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="c8263-118">Name of column.</span></span>

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

### <span data-ttu-id="c8263-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8263-119">-DatabaseName</span></span>
<span data-ttu-id="c8263-120">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="c8263-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="c8263-121">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="c8263-121">-DatabaseObject</span></span>
<span data-ttu-id="c8263-122">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="c8263-122">The SQL database object.</span></span>

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

### <span data-ttu-id="c8263-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8263-123">-DefaultProfile</span></span>
<span data-ttu-id="c8263-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8263-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8263-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c8263-125">-InputObject</span></span>
<span data-ttu-id="c8263-126">Obiekt reprezentujący klasyfikację wrażliwości bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="c8263-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="c8263-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8263-127">-PassThru</span></span>
<span data-ttu-id="c8263-128">Określa, czy ma być wyprowadzany model klasyfikacji wrażliwości na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8263-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="c8263-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8263-129">-ResourceGroupName</span></span>
<span data-ttu-id="c8263-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8263-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8263-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c8263-131">-SchemaName</span></span>
<span data-ttu-id="c8263-132">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="c8263-132">Name of schema.</span></span>

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

### <span data-ttu-id="c8263-133">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c8263-133">-ServerName</span></span>
<span data-ttu-id="c8263-134">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="c8263-134">SQL server name.</span></span>

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

### <span data-ttu-id="c8263-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="c8263-135">-TableName</span></span>
<span data-ttu-id="c8263-136">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="c8263-136">Name of table.</span></span>

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

### <span data-ttu-id="c8263-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8263-137">-Confirm</span></span>
<span data-ttu-id="c8263-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8263-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8263-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8263-139">-WhatIf</span></span>
<span data-ttu-id="c8263-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8263-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8263-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8263-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8263-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8263-142">CommonParameters</span></span>
<span data-ttu-id="c8263-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8263-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8263-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8263-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8263-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8263-145">INPUTS</span></span>

### <span data-ttu-id="c8263-146">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="c8263-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="c8263-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8263-147">OUTPUTS</span></span>

### <span data-ttu-id="c8263-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8263-148">System.Boolean</span></span>

## <span data-ttu-id="c8263-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8263-149">NOTES</span></span>

## <span data-ttu-id="c8263-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8263-150">RELATED LINKS</span></span>

[<span data-ttu-id="c8263-151">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c8263-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)