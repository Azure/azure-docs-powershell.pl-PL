---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c476f19f8c2ab8af334f92e75b67aeee151793fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707732"
---
# <span data-ttu-id="b2c55-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="b2c55-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="b2c55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2c55-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c55-103">Ustawia typy informacji i oznakowań liter kolumn w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c55-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b2c55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2c55-104">SYNTAX</span></span>

### <span data-ttu-id="b2c55-105">ClassificationObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2c55-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2c55-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2c55-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2c55-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2c55-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c55-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b2c55-108">DESCRIPTION</span></span>
<span data-ttu-id="b2c55-109">Polecenie cmdlet Set-AzSqlInstanceDatabaseSensitivityClassification ustawia typy informacji i etykiet liter kolumn w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c55-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b2c55-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2c55-110">EXAMPLES</span></span>

### <span data-ttu-id="b2c55-111">Przykład 1: Ustawianie typu informacji i etykiety wrażliwości kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c55-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="b2c55-112">Przykład 2: Ustawianie zalecanych typów informacji i etykiet wrażliwości kolumn w bazie danych wystąpień zarządzanych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c55-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="b2c55-113">Przykład 3: Ustawianie typu informacji i etykiety wrażliwości kolumny w bazie danych wystąpień zarządzanych SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="b2c55-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="b2c55-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2c55-114">PARAMETERS</span></span>

### <span data-ttu-id="b2c55-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2c55-115">-AsJob</span></span>
<span data-ttu-id="b2c55-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b2c55-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2c55-117">-Klasyfikacyjnobject</span><span class="sxs-lookup"><span data-stu-id="b2c55-117">-ClassificationObject</span></span>
<span data-ttu-id="b2c55-118">Obiekt reprezentujący klasyfikację wrażliwości bazy danych wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="b2c55-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c55-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b2c55-119">-ColumnName</span></span>
<span data-ttu-id="b2c55-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="b2c55-120">Name of column.</span></span>

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

### <span data-ttu-id="b2c55-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b2c55-121">-DatabaseName</span></span>
<span data-ttu-id="b2c55-122">Nazwa bazy danych wystąpienia zarządzanego w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b2c55-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="b2c55-123">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="b2c55-123">-DatabaseObject</span></span>
<span data-ttu-id="b2c55-124">Obiekt bazy danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c55-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c55-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c55-125">-DefaultProfile</span></span>
<span data-ttu-id="b2c55-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c55-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2c55-127">-Informationtype</span><span class="sxs-lookup"><span data-stu-id="b2c55-127">-InformationType</span></span>
<span data-ttu-id="b2c55-128">Nazwa opisująca typ informacji przechowywanych w kolumnie.</span><span class="sxs-lookup"><span data-stu-id="b2c55-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="b2c55-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b2c55-129">-InstanceName</span></span>
<span data-ttu-id="b2c55-130">Nazwa wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c55-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="b2c55-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2c55-131">-PassThru</span></span>
<span data-ttu-id="b2c55-132">Określa, czy ma być wyprowadzany model klasyfikacji wrażliwości na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2c55-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="b2c55-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2c55-133">-ResourceGroupName</span></span>
<span data-ttu-id="b2c55-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2c55-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2c55-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b2c55-135">-SchemaName</span></span>
<span data-ttu-id="b2c55-136">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="b2c55-136">Name of schema.</span></span>

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

### <span data-ttu-id="b2c55-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="b2c55-137">-SensitivityLabel</span></span>
<span data-ttu-id="b2c55-138">Nazwa opisująca wrażliwość danych przechowywanych w kolumnie.</span><span class="sxs-lookup"><span data-stu-id="b2c55-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="b2c55-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="b2c55-139">-TableName</span></span>
<span data-ttu-id="b2c55-140">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="b2c55-140">Name of table.</span></span>

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

### <span data-ttu-id="b2c55-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2c55-141">-Confirm</span></span>
<span data-ttu-id="b2c55-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2c55-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c55-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c55-143">-WhatIf</span></span>
<span data-ttu-id="b2c55-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2c55-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2c55-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b2c55-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c55-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c55-146">CommonParameters</span></span>
<span data-ttu-id="b2c55-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c55-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c55-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2c55-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c55-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2c55-149">INPUTS</span></span>

### <span data-ttu-id="b2c55-150">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b2c55-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="b2c55-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2c55-151">OUTPUTS</span></span>

### <span data-ttu-id="b2c55-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2c55-152">System.Boolean</span></span>

## <span data-ttu-id="b2c55-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2c55-153">NOTES</span></span>

## <span data-ttu-id="b2c55-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2c55-154">RELATED LINKS</span></span>

[<span data-ttu-id="b2c55-155">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b2c55-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
