---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c594a9bf247355201bc08e438af1d9dff8cd3f7d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369588"
---
# <span data-ttu-id="8b816-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="8b816-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="8b816-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b816-102">SYNOPSIS</span></span>
<span data-ttu-id="8b816-103">Usuwa typy informacji oraz etykiety liter kolumn w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8b816-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="8b816-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b816-104">SYNTAX</span></span>

### <span data-ttu-id="8b816-105">ClassificationObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8b816-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b816-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b816-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b816-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b816-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b816-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8b816-108">DESCRIPTION</span></span>
<span data-ttu-id="8b816-109">Polecenie cmdlet Remove-AzSqlInstanceDatabaseSensitivityClassification usuwa typy informacji oraz etykiety liter kolumn w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8b816-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="8b816-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b816-110">EXAMPLES</span></span>

### <span data-ttu-id="8b816-111">Przykład 1: usuwanie typu informacji i etykiety wrażliwości kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8b816-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="8b816-112">Przykład 2: usuwanie bieżących typów informacji i etykiet liter kolumn w bazie danych wystąpień zarządzanych SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="8b816-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="8b816-113">Przykład 3: usuwanie typu informacji i etykiety wrażliwości kolumny w bazie danych wystąpienia zarządzanego SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="8b816-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="8b816-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b816-114">PARAMETERS</span></span>

### <span data-ttu-id="8b816-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b816-115">-AsJob</span></span>
<span data-ttu-id="8b816-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8b816-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b816-117">-Klasyfikacyjnobject</span><span class="sxs-lookup"><span data-stu-id="8b816-117">-ClassificationObject</span></span>
<span data-ttu-id="8b816-118">Obiekt reprezentujący klasyfikację wrażliwości bazy danych wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="8b816-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="8b816-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="8b816-119">-ColumnName</span></span>
<span data-ttu-id="8b816-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="8b816-120">Name of column.</span></span>

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

### <span data-ttu-id="8b816-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8b816-121">-DatabaseName</span></span>
<span data-ttu-id="8b816-122">Nazwa bazy danych wystąpienia zarządzanego w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8b816-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="8b816-123">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="8b816-123">-DatabaseObject</span></span>
<span data-ttu-id="8b816-124">Obiekt bazy danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8b816-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="8b816-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b816-125">-DefaultProfile</span></span>
<span data-ttu-id="8b816-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b816-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b816-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8b816-127">-InstanceName</span></span>
<span data-ttu-id="8b816-128">Nazwa wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8b816-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="8b816-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b816-129">-PassThru</span></span>
<span data-ttu-id="8b816-130">Określa, czy ma być wyprowadzany model klasyfikacji wrażliwości na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b816-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="8b816-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b816-131">-ResourceGroupName</span></span>
<span data-ttu-id="8b816-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8b816-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="8b816-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8b816-133">-SchemaName</span></span>
<span data-ttu-id="8b816-134">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="8b816-134">Name of schema.</span></span>

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

### <span data-ttu-id="8b816-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="8b816-135">-TableName</span></span>
<span data-ttu-id="8b816-136">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="8b816-136">Name of table.</span></span>

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

### <span data-ttu-id="8b816-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b816-137">-Confirm</span></span>
<span data-ttu-id="8b816-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b816-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b816-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b816-139">-WhatIf</span></span>
<span data-ttu-id="8b816-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b816-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b816-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8b816-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b816-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b816-142">CommonParameters</span></span>
<span data-ttu-id="8b816-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b816-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b816-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b816-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b816-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b816-145">INPUTS</span></span>

### <span data-ttu-id="8b816-146">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="8b816-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="8b816-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b816-147">OUTPUTS</span></span>

### <span data-ttu-id="8b816-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b816-148">System.Boolean</span></span>

## <span data-ttu-id="8b816-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b816-149">NOTES</span></span>

## <span data-ttu-id="8b816-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b816-150">RELATED LINKS</span></span>

[<span data-ttu-id="8b816-151">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="8b816-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
