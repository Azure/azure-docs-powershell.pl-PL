---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: c9aef3a38cc210615a1f663d6d6104ae40f66245
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015873"
---
# <span data-ttu-id="47970-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="47970-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="47970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47970-102">SYNOPSIS</span></span>
<span data-ttu-id="47970-103">Włącza zalecenia wrażliwości dotyczące kolumn (zalecenia są domyślnie włączone we wszystkich kolumnach) w bazie danych azure SQL managed instance database.</span><span class="sxs-lookup"><span data-stu-id="47970-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="47970-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="47970-104">SYNTAX</span></span>

### <span data-ttu-id="47970-105">InputObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="47970-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47970-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="47970-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47970-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="47970-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47970-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="47970-108">DESCRIPTION</span></span>
<span data-ttu-id="47970-109">Polecenie Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet umożliwia wyświetlanie rekomendacji wrażliwości kolumn w bazie danych azure SQL managed instance database.</span><span class="sxs-lookup"><span data-stu-id="47970-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="47970-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="47970-110">EXAMPLES</span></span>

### <span data-ttu-id="47970-111">Przykład 1. Włączanie rekomendacji wrażliwości dla danej kolumny w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="47970-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="47970-112">Przykład 2. Włączanie rekomendacji wrażliwości dla danej kolumny w bazie danych azure SQL managed instance database za pomocą funkcji Piping.</span><span class="sxs-lookup"><span data-stu-id="47970-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="47970-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47970-113">PARAMETERS</span></span>

### <span data-ttu-id="47970-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="47970-114">-AsJob</span></span>
<span data-ttu-id="47970-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="47970-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47970-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="47970-116">-ColumnName</span></span>
<span data-ttu-id="47970-117">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="47970-117">Name of column.</span></span>

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

### <span data-ttu-id="47970-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47970-118">-DatabaseName</span></span>
<span data-ttu-id="47970-119">Nazwa bazy danych azure SQL managed instance database.</span><span class="sxs-lookup"><span data-stu-id="47970-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="47970-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="47970-120">-DatabaseObject</span></span>
<span data-ttu-id="47970-121">Obiekt bazy danych zarządzanych wystąpień sql platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47970-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="47970-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47970-122">-DefaultProfile</span></span>
<span data-ttu-id="47970-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="47970-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47970-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47970-124">-InputObject</span></span>
<span data-ttu-id="47970-125">Obiekt reprezentujący klasyfikację wrażliwości zarządzanego wystąpienia SQL.</span><span class="sxs-lookup"><span data-stu-id="47970-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47970-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="47970-126">-InstanceName</span></span>
<span data-ttu-id="47970-127">Nazwa zarządzanego wystąpienia języka SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47970-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="47970-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47970-128">-PassThru</span></span>
<span data-ttu-id="47970-129">Określa, czy model klasyfikacji wrażliwości ma być wyprowadzony na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47970-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="47970-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47970-130">-ResourceGroupName</span></span>
<span data-ttu-id="47970-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47970-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="47970-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="47970-132">-SchemaName</span></span>
<span data-ttu-id="47970-133">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="47970-133">Name of schema.</span></span>

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

### <span data-ttu-id="47970-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="47970-134">-TableName</span></span>
<span data-ttu-id="47970-135">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="47970-135">Name of table.</span></span>

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

### <span data-ttu-id="47970-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47970-136">-Confirm</span></span>
<span data-ttu-id="47970-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="47970-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47970-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47970-138">-WhatIf</span></span>
<span data-ttu-id="47970-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47970-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47970-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="47970-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47970-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47970-141">CommonParameters</span></span>
<span data-ttu-id="47970-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47970-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47970-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47970-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47970-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47970-144">INPUTS</span></span>

### <span data-ttu-id="47970-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="47970-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="47970-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47970-146">OUTPUTS</span></span>

### <span data-ttu-id="47970-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47970-147">System.Boolean</span></span>

## <span data-ttu-id="47970-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="47970-148">NOTES</span></span>

## <span data-ttu-id="47970-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47970-149">RELATED LINKS</span></span>

[<span data-ttu-id="47970-150">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="47970-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)