---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051921"
---
# <span data-ttu-id="1fdb8-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="1fdb8-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="1fdb8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fdb8-102">SYNOPSIS</span></span>
<span data-ttu-id="1fdb8-103">Wyłączenie (odrzucanie) rekomendacji dotyczących wrażliwości na kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="1fdb8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fdb8-104">SYNTAX</span></span>

### <span data-ttu-id="1fdb8-105">InputObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1fdb8-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fdb8-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fdb8-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fdb8-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fdb8-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fdb8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1fdb8-108">DESCRIPTION</span></span>
<span data-ttu-id="1fdb8-109">Polecenie cmdlet Disable-AzSqlInstanceDatabaseSensitivityRecommendation wyłącza zaleceń dotyczących wrażliwości na kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="1fdb8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fdb8-110">EXAMPLES</span></span>

### <span data-ttu-id="1fdb8-111">Przykład 1: wyłączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="1fdb8-112">Przykład 2: wyłączanie zaleceń dotyczących wrażliwości na kolumny, które mają rekomendacje dotyczące wrażliwości w bazie danych wystąpień zarządzanych SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="1fdb8-113">Przykład 3: wyłączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych wystąpienia zarządzanego SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="1fdb8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fdb8-114">PARAMETERS</span></span>

### <span data-ttu-id="1fdb8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fdb8-115">-AsJob</span></span>
<span data-ttu-id="1fdb8-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1fdb8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fdb8-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="1fdb8-117">-ColumnName</span></span>
<span data-ttu-id="1fdb8-118">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-118">Name of column.</span></span>

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

### <span data-ttu-id="1fdb8-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1fdb8-119">-DatabaseName</span></span>
<span data-ttu-id="1fdb8-120">Nazwa bazy danych wystąpienia zarządzanego w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="1fdb8-121">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="1fdb8-121">-DatabaseObject</span></span>
<span data-ttu-id="1fdb8-122">Obiekt bazy danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="1fdb8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fdb8-123">-DefaultProfile</span></span>
<span data-ttu-id="1fdb8-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fdb8-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1fdb8-125">-InputObject</span></span>
<span data-ttu-id="1fdb8-126">Obiekt reprezentujący klasyfikację wrażliwości bazy danych wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="1fdb8-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1fdb8-127">-InstanceName</span></span>
<span data-ttu-id="1fdb8-128">Nazwa wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="1fdb8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fdb8-129">-PassThru</span></span>
<span data-ttu-id="1fdb8-130">Określa, czy ma być wyprowadzany model klasyfikacji wrażliwości na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="1fdb8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fdb8-131">-ResourceGroupName</span></span>
<span data-ttu-id="1fdb8-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="1fdb8-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="1fdb8-133">-SchemaName</span></span>
<span data-ttu-id="1fdb8-134">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-134">Name of schema.</span></span>

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

### <span data-ttu-id="1fdb8-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="1fdb8-135">-TableName</span></span>
<span data-ttu-id="1fdb8-136">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-136">Name of table.</span></span>

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

### <span data-ttu-id="1fdb8-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1fdb8-137">-Confirm</span></span>
<span data-ttu-id="1fdb8-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fdb8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fdb8-139">-WhatIf</span></span>
<span data-ttu-id="1fdb8-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fdb8-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fdb8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fdb8-142">CommonParameters</span></span>
<span data-ttu-id="1fdb8-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fdb8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fdb8-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fdb8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fdb8-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fdb8-145">INPUTS</span></span>

### <span data-ttu-id="1fdb8-146">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="1fdb8-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="1fdb8-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fdb8-147">OUTPUTS</span></span>

### <span data-ttu-id="1fdb8-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fdb8-148">System.Boolean</span></span>

## <span data-ttu-id="1fdb8-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fdb8-149">NOTES</span></span>

## <span data-ttu-id="1fdb8-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fdb8-150">RELATED LINKS</span></span>

[<span data-ttu-id="1fdb8-151">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="1fdb8-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)