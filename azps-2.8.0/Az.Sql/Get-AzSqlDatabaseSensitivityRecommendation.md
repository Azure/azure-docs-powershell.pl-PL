---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: ba8229bcddf27a2a14d50efc2cbd32e6e47015c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887014"
---
# <span data-ttu-id="63fcd-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="63fcd-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="63fcd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="63fcd-103">Pobiera Polecane typy informacji oraz etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="63fcd-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="63fcd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63fcd-104">SYNTAX</span></span>

### <span data-ttu-id="63fcd-105">DatabaseObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63fcd-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63fcd-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="63fcd-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63fcd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63fcd-107">DESCRIPTION</span></span>
<span data-ttu-id="63fcd-108">Polecenie cmdlet Get-AzSqlDatabaseSensitivityRecommendation zwraca Polecane typy informacji oraz etykiety liter kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="63fcd-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="63fcd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63fcd-109">EXAMPLES</span></span>

### <span data-ttu-id="63fcd-110">Przykład 1: uzyskiwanie zalecanych typów informacji i etykiet wrażliwości bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="63fcd-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
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

### <span data-ttu-id="63fcd-111">Przykład 2: uzyskiwanie zalecanych typów informacji i etykiet wrażliwości bazy danych SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="63fcd-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
ServerName        : server
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

## <span data-ttu-id="63fcd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63fcd-112">PARAMETERS</span></span>

### <span data-ttu-id="63fcd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63fcd-113">-AsJob</span></span>
<span data-ttu-id="63fcd-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="63fcd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63fcd-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63fcd-115">-DatabaseName</span></span>
<span data-ttu-id="63fcd-116">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="63fcd-116">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="63fcd-117">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="63fcd-117">-DatabaseObject</span></span>
<span data-ttu-id="63fcd-118">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="63fcd-118">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63fcd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fcd-119">-DefaultProfile</span></span>
<span data-ttu-id="63fcd-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63fcd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63fcd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63fcd-121">-ResourceGroupName</span></span>
<span data-ttu-id="63fcd-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="63fcd-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="63fcd-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="63fcd-123">-ServerName</span></span>
<span data-ttu-id="63fcd-124">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="63fcd-124">SQL server name.</span></span>

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

### <span data-ttu-id="63fcd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fcd-125">CommonParameters</span></span>
<span data-ttu-id="63fcd-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63fcd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fcd-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63fcd-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fcd-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63fcd-128">INPUTS</span></span>

### <span data-ttu-id="63fcd-129">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="63fcd-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="63fcd-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63fcd-130">OUTPUTS</span></span>

### <span data-ttu-id="63fcd-131">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="63fcd-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="63fcd-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63fcd-132">NOTES</span></span>

## <span data-ttu-id="63fcd-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63fcd-133">RELATED LINKS</span></span>

[<span data-ttu-id="63fcd-134">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="63fcd-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
