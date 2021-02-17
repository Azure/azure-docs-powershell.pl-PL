---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196195"
---
# <span data-ttu-id="9bc7a-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="9bc7a-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="9bc7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bc7a-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc7a-103">Wyłącza (odrzuca) zalecenia dotyczące wrażliwości kolumn w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="9bc7a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9bc7a-104">SYNTAX</span></span>

### <span data-ttu-id="9bc7a-105">InputObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9bc7a-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bc7a-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bc7a-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bc7a-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bc7a-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bc7a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9bc7a-108">DESCRIPTION</span></span>
<span data-ttu-id="9bc7a-109">Polecenie Disable-AzSqlInstanceDatabaseSensitivityRecommendation wyłącza (odrzuca) zalecenia dotyczące wrażliwości kolumn w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="9bc7a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9bc7a-110">EXAMPLES</span></span>

### <span data-ttu-id="9bc7a-111">Przykład 1. Wyłącz zalecenia dotyczące wrażliwości dla danej kolumny w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="9bc7a-112">Przykład 2. Wyłącz zalecenia dotyczące wrażliwości kolumn, które mają zalecenia wrażliwości w bazie danych zarządzanych wystąpień języka SQL Azure za pomocą funkcji Piping.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="9bc7a-113">Przykład 3. Wyłącz zalecenia dotyczące wrażliwości dla danej kolumny w bazie danych azure SQL managed instance database za pomocą funkcji Piping.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="9bc7a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bc7a-114">PARAMETERS</span></span>

### <span data-ttu-id="9bc7a-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9bc7a-115">-AsJob</span></span>
<span data-ttu-id="9bc7a-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9bc7a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bc7a-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9bc7a-117">-ColumnName</span></span>
<span data-ttu-id="9bc7a-118">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-118">Name of column.</span></span>

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

### <span data-ttu-id="9bc7a-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9bc7a-119">-DatabaseName</span></span>
<span data-ttu-id="9bc7a-120">Nazwa bazy danych azure SQL managed instance database.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="9bc7a-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9bc7a-121">-DatabaseObject</span></span>
<span data-ttu-id="9bc7a-122">Obiekt bazy danych zarządzanych wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="9bc7a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc7a-123">-DefaultProfile</span></span>
<span data-ttu-id="9bc7a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bc7a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bc7a-125">-InputObject</span></span>
<span data-ttu-id="9bc7a-126">Obiekt reprezentujący klasyfikację wrażliwości zarządzanego wystąpienia SQL.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="9bc7a-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9bc7a-127">-InstanceName</span></span>
<span data-ttu-id="9bc7a-128">Nazwa zarządzanego wystąpienia języka SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="9bc7a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bc7a-129">-PassThru</span></span>
<span data-ttu-id="9bc7a-130">Określa, czy model klasyfikacji wrażliwości ma być wyprowadzony na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9bc7a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bc7a-131">-ResourceGroupName</span></span>
<span data-ttu-id="9bc7a-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="9bc7a-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9bc7a-133">-SchemaName</span></span>
<span data-ttu-id="9bc7a-134">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-134">Name of schema.</span></span>

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

### <span data-ttu-id="9bc7a-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="9bc7a-135">-TableName</span></span>
<span data-ttu-id="9bc7a-136">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-136">Name of table.</span></span>

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

### <span data-ttu-id="9bc7a-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9bc7a-137">-Confirm</span></span>
<span data-ttu-id="9bc7a-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bc7a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bc7a-139">-WhatIf</span></span>
<span data-ttu-id="9bc7a-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bc7a-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bc7a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc7a-142">CommonParameters</span></span>
<span data-ttu-id="9bc7a-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc7a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc7a-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bc7a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc7a-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bc7a-145">INPUTS</span></span>

### <span data-ttu-id="9bc7a-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9bc7a-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9bc7a-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9bc7a-147">OUTPUTS</span></span>

### <span data-ttu-id="9bc7a-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9bc7a-148">System.Boolean</span></span>

## <span data-ttu-id="9bc7a-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9bc7a-149">NOTES</span></span>

## <span data-ttu-id="9bc7a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bc7a-150">RELATED LINKS</span></span>

[<span data-ttu-id="9bc7a-151">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="9bc7a-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)