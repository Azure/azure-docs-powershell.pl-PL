---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895925"
---
# <span data-ttu-id="0d1c5-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="0d1c5-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="0d1c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1c5-103">Włączanie rekomendacji dotyczących wrażliwości na kolumny (rekomendacje są domyślnie włączone we wszystkich kolumnach) w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="0d1c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d1c5-104">SYNTAX</span></span>

### <span data-ttu-id="0d1c5-105">InputObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0d1c5-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c5-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d1c5-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c5-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d1c5-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d1c5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0d1c5-108">DESCRIPTION</span></span>
<span data-ttu-id="0d1c5-109">Polecenie cmdlet Enable-AzSqlInstanceDatabaseSensitivityRecommendation włącza rekomendacje dotyczące wrażliwości na kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="0d1c5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d1c5-110">EXAMPLES</span></span>

### <span data-ttu-id="0d1c5-111">Przykład 1: Włączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="0d1c5-112">Przykład 2: Włączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych wystąpienia zarządzanego SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="0d1c5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d1c5-113">PARAMETERS</span></span>

### <span data-ttu-id="0d1c5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d1c5-114">-AsJob</span></span>
<span data-ttu-id="0d1c5-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0d1c5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d1c5-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0d1c5-116">-ColumnName</span></span>
<span data-ttu-id="0d1c5-117">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-117">Name of column.</span></span>

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

### <span data-ttu-id="0d1c5-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d1c5-118">-DatabaseName</span></span>
<span data-ttu-id="0d1c5-119">Nazwa bazy danych wystąpienia zarządzanego w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="0d1c5-120">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="0d1c5-120">-DatabaseObject</span></span>
<span data-ttu-id="0d1c5-121">Obiekt bazy danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="0d1c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1c5-122">-DefaultProfile</span></span>
<span data-ttu-id="0d1c5-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d1c5-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d1c5-124">-InputObject</span></span>
<span data-ttu-id="0d1c5-125">Obiekt reprezentujący klasyfikację wrażliwości bazy danych wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="0d1c5-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0d1c5-126">-InstanceName</span></span>
<span data-ttu-id="0d1c5-127">Nazwa wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="0d1c5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d1c5-128">-PassThru</span></span>
<span data-ttu-id="0d1c5-129">Określa, czy ma być wyprowadzany model klasyfikacji wrażliwości na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="0d1c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1c5-130">-ResourceGroupName</span></span>
<span data-ttu-id="0d1c5-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="0d1c5-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0d1c5-132">-SchemaName</span></span>
<span data-ttu-id="0d1c5-133">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-133">Name of schema.</span></span>

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

### <span data-ttu-id="0d1c5-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="0d1c5-134">-TableName</span></span>
<span data-ttu-id="0d1c5-135">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-135">Name of table.</span></span>

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

### <span data-ttu-id="0d1c5-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d1c5-136">-Confirm</span></span>
<span data-ttu-id="0d1c5-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d1c5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d1c5-138">-WhatIf</span></span>
<span data-ttu-id="0d1c5-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d1c5-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d1c5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1c5-141">CommonParameters</span></span>
<span data-ttu-id="0d1c5-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d1c5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1c5-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d1c5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1c5-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d1c5-144">INPUTS</span></span>

### <span data-ttu-id="0d1c5-145">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="0d1c5-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="0d1c5-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d1c5-146">OUTPUTS</span></span>

### <span data-ttu-id="0d1c5-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d1c5-147">System.Boolean</span></span>

## <span data-ttu-id="0d1c5-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d1c5-148">NOTES</span></span>

## <span data-ttu-id="0d1c5-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d1c5-149">RELATED LINKS</span></span>

[<span data-ttu-id="0d1c5-150">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="0d1c5-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)