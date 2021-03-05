---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 9a33504fb27d7c1cf623b03f6c4ea8fefb32c85f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999409"
---
# <span data-ttu-id="3bc64-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="3bc64-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="3bc64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bc64-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc64-103">Pobiera bieżące typy informacji i etykiety wrażliwości kolumn w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="3bc64-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="3bc64-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3bc64-104">SYNTAX</span></span>

### <span data-ttu-id="3bc64-105">DatabaseObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3bc64-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc64-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc64-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc64-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc64-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc64-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc64-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bc64-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="3bc64-109">DESCRIPTION</span></span>
<span data-ttu-id="3bc64-110">Polecenie Get-AzSqlInstanceDatabaseSensitivityClassification zwraca bieżące typy informacji i etykiety wrażliwości kolumn w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="3bc64-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="3bc64-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3bc64-111">EXAMPLES</span></span>

### <span data-ttu-id="3bc64-112">Przykład 1. Pobierz bieżące typy informacji i etykiety wrażliwości bazy danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="3bc64-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="3bc64-113">Przykład 2. Uzyskiwanie bieżących typów informacji i etykiet wrażliwości w bazie danych azure SQL managed Instance za pomocą funkcji Piping.</span><span class="sxs-lookup"><span data-stu-id="3bc64-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="3bc64-114">Przykład 3. Pobierz bieżący typ informacji i etykietę wrażliwości konkretnej kolumny bazy danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="3bc64-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="3bc64-115">Przykład 4. Pobierz bieżący typ informacji i etykietę wrażliwości określonej kolumny bazy danych azure SQL managed instance database za pomocą połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="3bc64-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="3bc64-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bc64-116">PARAMETERS</span></span>

### <span data-ttu-id="3bc64-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3bc64-117">-AsJob</span></span>
<span data-ttu-id="3bc64-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3bc64-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3bc64-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3bc64-119">-ColumnName</span></span>
<span data-ttu-id="3bc64-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="3bc64-120">Name of column.</span></span>

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

### <span data-ttu-id="3bc64-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3bc64-121">-DatabaseName</span></span>
<span data-ttu-id="3bc64-122">Nazwa bazy danych azure SQL managed instance database.</span><span class="sxs-lookup"><span data-stu-id="3bc64-122">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc64-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="3bc64-123">-DatabaseObject</span></span>
<span data-ttu-id="3bc64-124">Obiekt bazy danych zarządzanych wystąpień sql platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc64-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc64-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc64-125">-DefaultProfile</span></span>
<span data-ttu-id="3bc64-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc64-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc64-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3bc64-127">-InstanceName</span></span>
<span data-ttu-id="3bc64-128">Nazwa zarządzanego wystąpienia języka SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc64-128">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc64-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc64-129">-ResourceGroupName</span></span>
<span data-ttu-id="3bc64-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3bc64-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc64-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3bc64-131">-SchemaName</span></span>
<span data-ttu-id="3bc64-132">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="3bc64-132">Name of schema.</span></span>

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

### <span data-ttu-id="3bc64-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="3bc64-133">-TableName</span></span>
<span data-ttu-id="3bc64-134">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="3bc64-134">Name of table.</span></span>

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

### <span data-ttu-id="3bc64-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc64-135">CommonParameters</span></span>
<span data-ttu-id="3bc64-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc64-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc64-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bc64-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc64-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bc64-138">INPUTS</span></span>

### <span data-ttu-id="3bc64-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3bc64-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="3bc64-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bc64-140">OUTPUTS</span></span>

### <span data-ttu-id="3bc64-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="3bc64-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="3bc64-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3bc64-142">NOTES</span></span>

## <span data-ttu-id="3bc64-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bc64-143">RELATED LINKS</span></span>

[<span data-ttu-id="3bc64-144">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="3bc64-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
