---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062046"
---
# <span data-ttu-id="4897d-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="4897d-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="4897d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4897d-102">SYNOPSIS</span></span>
<span data-ttu-id="4897d-103">Włączanie rekomendacji dotyczących wrażliwości na kolumny (rekomendacje są domyślnie włączone we wszystkich kolumnach) w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4897d-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="4897d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4897d-104">SYNTAX</span></span>

### <span data-ttu-id="4897d-105">InputObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4897d-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4897d-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4897d-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4897d-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4897d-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4897d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4897d-108">DESCRIPTION</span></span>
<span data-ttu-id="4897d-109">Polecenie cmdlet Enable-AzSqlInstanceDatabaseSensitivityRecommendation włącza rekomendacje dotyczące wrażliwości na kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4897d-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="4897d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4897d-110">EXAMPLES</span></span>

### <span data-ttu-id="4897d-111">Przykład 1: Włączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4897d-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="4897d-112">Przykład 2: Włączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych wystąpienia zarządzanego SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="4897d-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="4897d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4897d-113">PARAMETERS</span></span>

### <span data-ttu-id="4897d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4897d-114">-AsJob</span></span>
<span data-ttu-id="4897d-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4897d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4897d-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4897d-116">-ColumnName</span></span>
<span data-ttu-id="4897d-117">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="4897d-117">Name of column.</span></span>

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

### <span data-ttu-id="4897d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4897d-118">-DatabaseName</span></span>
<span data-ttu-id="4897d-119">Nazwa bazy danych wystąpienia zarządzanego w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4897d-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="4897d-120">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="4897d-120">-DatabaseObject</span></span>
<span data-ttu-id="4897d-121">Obiekt bazy danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4897d-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="4897d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4897d-122">-DefaultProfile</span></span>
<span data-ttu-id="4897d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4897d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4897d-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4897d-124">-InputObject</span></span>
<span data-ttu-id="4897d-125">Obiekt reprezentujący klasyfikację wrażliwości bazy danych wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="4897d-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="4897d-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4897d-126">-InstanceName</span></span>
<span data-ttu-id="4897d-127">Nazwa wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4897d-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="4897d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4897d-128">-PassThru</span></span>
<span data-ttu-id="4897d-129">Określa, czy ma być wyprowadzany model klasyfikacji wrażliwości na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4897d-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="4897d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4897d-130">-ResourceGroupName</span></span>
<span data-ttu-id="4897d-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4897d-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="4897d-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4897d-132">-SchemaName</span></span>
<span data-ttu-id="4897d-133">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="4897d-133">Name of schema.</span></span>

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

### <span data-ttu-id="4897d-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="4897d-134">-TableName</span></span>
<span data-ttu-id="4897d-135">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="4897d-135">Name of table.</span></span>

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

### <span data-ttu-id="4897d-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4897d-136">-Confirm</span></span>
<span data-ttu-id="4897d-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4897d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4897d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4897d-138">-WhatIf</span></span>
<span data-ttu-id="4897d-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4897d-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4897d-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4897d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4897d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4897d-141">CommonParameters</span></span>
<span data-ttu-id="4897d-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4897d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4897d-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4897d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4897d-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4897d-144">INPUTS</span></span>

### <span data-ttu-id="4897d-145">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="4897d-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="4897d-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4897d-146">OUTPUTS</span></span>

### <span data-ttu-id="4897d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4897d-147">System.Boolean</span></span>

## <span data-ttu-id="4897d-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4897d-148">NOTES</span></span>

## <span data-ttu-id="4897d-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4897d-149">RELATED LINKS</span></span>

[<span data-ttu-id="4897d-150">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="4897d-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)