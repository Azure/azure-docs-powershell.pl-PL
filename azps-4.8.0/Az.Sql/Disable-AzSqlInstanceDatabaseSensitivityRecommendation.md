---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064724"
---
# <span data-ttu-id="a2a81-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="a2a81-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="a2a81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2a81-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a81-103">Wyłączenie (odrzucanie) rekomendacji dotyczących wrażliwości na kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a81-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a2a81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2a81-104">SYNTAX</span></span>

### <span data-ttu-id="a2a81-105">InputObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2a81-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2a81-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2a81-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2a81-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2a81-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2a81-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a2a81-108">DESCRIPTION</span></span>
<span data-ttu-id="a2a81-109">Polecenie cmdlet Disable-AzSqlInstanceDatabaseSensitivityRecommendation wyłącza zaleceń dotyczących wrażliwości na kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a81-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a2a81-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2a81-110">EXAMPLES</span></span>

### <span data-ttu-id="a2a81-111">Przykład 1: wyłączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a81-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="a2a81-112">Przykład 2: wyłączanie zaleceń dotyczących wrażliwości na kolumny, które mają rekomendacje dotyczące wrażliwości w bazie danych wystąpień zarządzanych SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="a2a81-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="a2a81-113">Przykład 3: wyłączanie rekomendacji dotyczących wrażliwości dla danej kolumny w bazie danych wystąpienia zarządzanego SQL Azure z potokiem.</span><span class="sxs-lookup"><span data-stu-id="a2a81-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="a2a81-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2a81-114">PARAMETERS</span></span>

### <span data-ttu-id="a2a81-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2a81-115">-AsJob</span></span>
<span data-ttu-id="a2a81-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a2a81-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2a81-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a2a81-117">-ColumnName</span></span>
<span data-ttu-id="a2a81-118">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="a2a81-118">Name of column.</span></span>

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

### <span data-ttu-id="a2a81-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2a81-119">-DatabaseName</span></span>
<span data-ttu-id="a2a81-120">Nazwa bazy danych wystąpienia zarządzanego w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a2a81-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="a2a81-121">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="a2a81-121">-DatabaseObject</span></span>
<span data-ttu-id="a2a81-122">Obiekt bazy danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a81-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="a2a81-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a81-123">-DefaultProfile</span></span>
<span data-ttu-id="a2a81-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a81-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2a81-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a2a81-125">-InputObject</span></span>
<span data-ttu-id="a2a81-126">Obiekt reprezentujący klasyfikację wrażliwości bazy danych wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="a2a81-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="a2a81-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a2a81-127">-InstanceName</span></span>
<span data-ttu-id="a2a81-128">Nazwa wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a81-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="a2a81-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2a81-129">-PassThru</span></span>
<span data-ttu-id="a2a81-130">Określa, czy ma być wyprowadzany model klasyfikacji wrażliwości na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2a81-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="a2a81-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2a81-131">-ResourceGroupName</span></span>
<span data-ttu-id="a2a81-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a2a81-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2a81-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a2a81-133">-SchemaName</span></span>
<span data-ttu-id="a2a81-134">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="a2a81-134">Name of schema.</span></span>

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

### <span data-ttu-id="a2a81-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="a2a81-135">-TableName</span></span>
<span data-ttu-id="a2a81-136">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="a2a81-136">Name of table.</span></span>

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

### <span data-ttu-id="a2a81-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2a81-137">-Confirm</span></span>
<span data-ttu-id="a2a81-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2a81-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2a81-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2a81-139">-WhatIf</span></span>
<span data-ttu-id="a2a81-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2a81-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2a81-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a2a81-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2a81-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a81-142">CommonParameters</span></span>
<span data-ttu-id="a2a81-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2a81-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a81-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2a81-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a81-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2a81-145">INPUTS</span></span>

### <span data-ttu-id="a2a81-146">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="a2a81-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="a2a81-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2a81-147">OUTPUTS</span></span>

### <span data-ttu-id="a2a81-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2a81-148">System.Boolean</span></span>

## <span data-ttu-id="a2a81-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2a81-149">NOTES</span></span>

## <span data-ttu-id="a2a81-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2a81-150">RELATED LINKS</span></span>

[<span data-ttu-id="a2a81-151">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a2a81-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)