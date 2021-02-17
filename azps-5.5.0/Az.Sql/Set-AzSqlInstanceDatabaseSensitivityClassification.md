---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: f524c8b30f609cb2fef3fb3f59550078b26b11b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243258"
---
# <span data-ttu-id="63166-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="63166-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="63166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63166-102">SYNOPSIS</span></span>
<span data-ttu-id="63166-103">Ustawia typy informacji i etykiety wrażliwości kolumn w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="63166-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="63166-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="63166-104">SYNTAX</span></span>

### <span data-ttu-id="63166-105">ClassificationObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="63166-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63166-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="63166-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63166-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="63166-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63166-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="63166-108">DESCRIPTION</span></span>
<span data-ttu-id="63166-109">Polecenie Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet ustawia typy informacji i etykiety wrażliwości kolumn w bazie danych azure SQL managed instance database.</span><span class="sxs-lookup"><span data-stu-id="63166-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="63166-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="63166-110">EXAMPLES</span></span>

### <span data-ttu-id="63166-111">Przykład 1. Ustawianie typu informacji i etykiety wrażliwości kolumny w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="63166-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="63166-112">Przykład 2. Ustawianie zalecanych typów informacji i etykiet wrażliwości kolumn w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="63166-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="63166-113">Przykład 3. Ustawianie typu informacji i etykiety wrażliwości kolumny w bazie danych zarządzanych wystąpień języka SQL Azure przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="63166-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="63166-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63166-114">PARAMETERS</span></span>

### <span data-ttu-id="63166-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="63166-115">-AsJob</span></span>
<span data-ttu-id="63166-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="63166-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63166-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="63166-117">-ClassificationObject</span></span>
<span data-ttu-id="63166-118">Obiekt reprezentujący klasyfikację wrażliwości zarządzanego wystąpienia SQL.</span><span class="sxs-lookup"><span data-stu-id="63166-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="63166-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="63166-119">-ColumnName</span></span>
<span data-ttu-id="63166-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="63166-120">Name of column.</span></span>

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

### <span data-ttu-id="63166-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63166-121">-DatabaseName</span></span>
<span data-ttu-id="63166-122">Nazwa bazy danych azure SQL managed instance database.</span><span class="sxs-lookup"><span data-stu-id="63166-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="63166-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="63166-123">-DatabaseObject</span></span>
<span data-ttu-id="63166-124">Obiekt bazy danych zarządzanych wystąpień sql platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="63166-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="63166-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63166-125">-DefaultProfile</span></span>
<span data-ttu-id="63166-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="63166-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63166-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="63166-127">-InformationType</span></span>
<span data-ttu-id="63166-128">Nazwa opisującą typ informacji przechowywanych w kolumnie.</span><span class="sxs-lookup"><span data-stu-id="63166-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="63166-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="63166-129">-InstanceName</span></span>
<span data-ttu-id="63166-130">Nazwa zarządzanego wystąpienia języka SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="63166-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="63166-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63166-131">-PassThru</span></span>
<span data-ttu-id="63166-132">Określa, czy model klasyfikacji wrażliwości ma być wyprowadzony na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63166-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="63166-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63166-133">-ResourceGroupName</span></span>
<span data-ttu-id="63166-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="63166-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="63166-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="63166-135">-SchemaName</span></span>
<span data-ttu-id="63166-136">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="63166-136">Name of schema.</span></span>

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

### <span data-ttu-id="63166-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="63166-137">-SensitivityLabel</span></span>
<span data-ttu-id="63166-138">Nazwa opisującą charakter danych przechowywanych w kolumnie.</span><span class="sxs-lookup"><span data-stu-id="63166-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="63166-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="63166-139">-TableName</span></span>
<span data-ttu-id="63166-140">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="63166-140">Name of table.</span></span>

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

### <span data-ttu-id="63166-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63166-141">-Confirm</span></span>
<span data-ttu-id="63166-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="63166-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63166-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63166-143">-WhatIf</span></span>
<span data-ttu-id="63166-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63166-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63166-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="63166-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63166-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63166-146">CommonParameters</span></span>
<span data-ttu-id="63166-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63166-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63166-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63166-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63166-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63166-149">INPUTS</span></span>

### <span data-ttu-id="63166-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="63166-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="63166-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63166-151">OUTPUTS</span></span>

### <span data-ttu-id="63166-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63166-152">System.Boolean</span></span>

## <span data-ttu-id="63166-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="63166-153">NOTES</span></span>

## <span data-ttu-id="63166-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63166-154">RELATED LINKS</span></span>

[<span data-ttu-id="63166-155">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="63166-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
