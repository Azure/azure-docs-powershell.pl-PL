---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 369a9f0f9bb475d27512eb13047a5a4ffe334573
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967441"
---
# <span data-ttu-id="0744b-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="0744b-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="0744b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0744b-102">SYNOPSIS</span></span>
<span data-ttu-id="0744b-103">Usuwa typy informacji i etykiety wrażliwości kolumn w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="0744b-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="0744b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0744b-104">SYNTAX</span></span>

### <span data-ttu-id="0744b-105">ClassificationObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0744b-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0744b-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0744b-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0744b-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0744b-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0744b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0744b-108">DESCRIPTION</span></span>
<span data-ttu-id="0744b-109">Polecenie Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet usuwa typy informacji i etykiety wrażliwości kolumn w bazie danych azure SQL managed instance database.</span><span class="sxs-lookup"><span data-stu-id="0744b-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="0744b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0744b-110">EXAMPLES</span></span>

### <span data-ttu-id="0744b-111">Przykład 1. Usuwanie typu informacji i etykiety wrażliwości kolumny w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="0744b-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="0744b-112">Przykład 2. Usuwanie bieżących typów informacji i etykiet wrażliwości kolumn w bazie danych azure SQL managed instance database za pomocą funkcji Piping.</span><span class="sxs-lookup"><span data-stu-id="0744b-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="0744b-113">Przykład 3. Usuwanie typu informacji i etykiety wrażliwości kolumny w bazie danych zarządzanych wystąpień sql platformy Azure za pomocą funkcji Piping.</span><span class="sxs-lookup"><span data-stu-id="0744b-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="0744b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0744b-114">PARAMETERS</span></span>

### <span data-ttu-id="0744b-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0744b-115">-AsJob</span></span>
<span data-ttu-id="0744b-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0744b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0744b-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="0744b-117">-ClassificationObject</span></span>
<span data-ttu-id="0744b-118">Obiekt reprezentujący klasyfikację wrażliwości zarządzanego wystąpienia SQL.</span><span class="sxs-lookup"><span data-stu-id="0744b-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="0744b-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0744b-119">-ColumnName</span></span>
<span data-ttu-id="0744b-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="0744b-120">Name of column.</span></span>

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

### <span data-ttu-id="0744b-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0744b-121">-DatabaseName</span></span>
<span data-ttu-id="0744b-122">Nazwa bazy danych azure SQL managed instance database.</span><span class="sxs-lookup"><span data-stu-id="0744b-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="0744b-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="0744b-123">-DatabaseObject</span></span>
<span data-ttu-id="0744b-124">Obiekt bazy danych zarządzanych wystąpień sql platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0744b-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="0744b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0744b-125">-DefaultProfile</span></span>
<span data-ttu-id="0744b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0744b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0744b-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0744b-127">-InstanceName</span></span>
<span data-ttu-id="0744b-128">Nazwa zarządzanego wystąpienia języka SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0744b-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="0744b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0744b-129">-PassThru</span></span>
<span data-ttu-id="0744b-130">Określa, czy model klasyfikacji wrażliwości ma być wyprowadzony na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0744b-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="0744b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0744b-131">-ResourceGroupName</span></span>
<span data-ttu-id="0744b-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0744b-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="0744b-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0744b-133">-SchemaName</span></span>
<span data-ttu-id="0744b-134">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="0744b-134">Name of schema.</span></span>

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

### <span data-ttu-id="0744b-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="0744b-135">-TableName</span></span>
<span data-ttu-id="0744b-136">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="0744b-136">Name of table.</span></span>

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

### <span data-ttu-id="0744b-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0744b-137">-Confirm</span></span>
<span data-ttu-id="0744b-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0744b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0744b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0744b-139">-WhatIf</span></span>
<span data-ttu-id="0744b-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0744b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0744b-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0744b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0744b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0744b-142">CommonParameters</span></span>
<span data-ttu-id="0744b-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0744b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0744b-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0744b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0744b-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0744b-145">INPUTS</span></span>

### <span data-ttu-id="0744b-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="0744b-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="0744b-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0744b-147">OUTPUTS</span></span>

### <span data-ttu-id="0744b-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0744b-148">System.Boolean</span></span>

## <span data-ttu-id="0744b-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0744b-149">NOTES</span></span>

## <span data-ttu-id="0744b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0744b-150">RELATED LINKS</span></span>

[<span data-ttu-id="0744b-151">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="0744b-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
