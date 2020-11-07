---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: d5923be20fd893aefee4e9a5789c2f6f57f20fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707931"
---
# <span data-ttu-id="a8972-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="a8972-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="a8972-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8972-102">SYNOPSIS</span></span>
<span data-ttu-id="a8972-103">Pobiera Polecane typy informacji i etykiety wrażliwości kolumn w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a8972-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a8972-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8972-104">SYNTAX</span></span>

### <span data-ttu-id="a8972-105">DatabaseObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a8972-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8972-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8972-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8972-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a8972-107">DESCRIPTION</span></span>
<span data-ttu-id="a8972-108">Polecenie cmdlet Get-AzSqlInstanceDatabaseSensitivityRecommendation zwraca Polecane typy informacji oraz etykiety liter kolumn w bazie danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a8972-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a8972-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8972-109">EXAMPLES</span></span>

### <span data-ttu-id="a8972-110">Przykład 1: uzyskiwanie zalecanych typów informacji i etykiet wrażliwości bazy danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a8972-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="a8972-111">Przykład 2: uzyskiwanie zalecanych typów informacji i etykiet wrażliwości bazy danych wystąpienia zarządzanego SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="a8972-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

## <span data-ttu-id="a8972-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8972-112">PARAMETERS</span></span>

### <span data-ttu-id="a8972-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8972-113">-AsJob</span></span>
<span data-ttu-id="a8972-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a8972-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8972-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a8972-115">-DatabaseName</span></span>
<span data-ttu-id="a8972-116">Nazwa bazy danych wystąpienia zarządzanego w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a8972-116">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8972-117">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="a8972-117">-DatabaseObject</span></span>
<span data-ttu-id="a8972-118">Obiekt bazy danych wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a8972-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8972-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8972-119">-DefaultProfile</span></span>
<span data-ttu-id="a8972-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8972-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8972-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a8972-121">-InstanceName</span></span>
<span data-ttu-id="a8972-122">Nazwa wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a8972-122">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8972-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8972-123">-ResourceGroupName</span></span>
<span data-ttu-id="a8972-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8972-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8972-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8972-125">CommonParameters</span></span>
<span data-ttu-id="a8972-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8972-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8972-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8972-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8972-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8972-128">INPUTS</span></span>

### <span data-ttu-id="a8972-129">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a8972-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a8972-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8972-130">OUTPUTS</span></span>

### <span data-ttu-id="a8972-131">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="a8972-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="a8972-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8972-132">NOTES</span></span>

## <span data-ttu-id="a8972-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8972-133">RELATED LINKS</span></span>

[<span data-ttu-id="a8972-134">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a8972-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
