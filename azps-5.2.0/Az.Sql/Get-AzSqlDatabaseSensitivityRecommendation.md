---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f002dca1c91ada808acc81108d3f06e9376a8b3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372010"
---
# <span data-ttu-id="b3d95-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="b3d95-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="b3d95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3d95-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d95-103">Pobiera Polecane typy informacji oraz etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="b3d95-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="b3d95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3d95-104">SYNTAX</span></span>

### <span data-ttu-id="b3d95-105">DatabaseObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3d95-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3d95-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3d95-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3d95-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b3d95-107">DESCRIPTION</span></span>
<span data-ttu-id="b3d95-108">Polecenie cmdlet Get-AzSqlDatabaseSensitivityRecommendation zwraca Polecane typy informacji oraz etykiety liter kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="b3d95-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="b3d95-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3d95-109">EXAMPLES</span></span>

### <span data-ttu-id="b3d95-110">Przykład 1: uzyskiwanie zalecanych typów informacji i etykiet wrażliwości bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b3d95-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
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

### <span data-ttu-id="b3d95-111">Przykład 2: uzyskiwanie zalecanych typów informacji i etykiet wrażliwości bazy danych SQL Azure przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="b3d95-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
ServerName        : server
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

## <span data-ttu-id="b3d95-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3d95-112">PARAMETERS</span></span>

### <span data-ttu-id="b3d95-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3d95-113">-AsJob</span></span>
<span data-ttu-id="b3d95-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b3d95-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3d95-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3d95-115">-DatabaseName</span></span>
<span data-ttu-id="b3d95-116">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="b3d95-116">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="b3d95-117">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="b3d95-117">-DatabaseObject</span></span>
<span data-ttu-id="b3d95-118">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b3d95-118">The SQL database object.</span></span>

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

### <span data-ttu-id="b3d95-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d95-119">-DefaultProfile</span></span>
<span data-ttu-id="b3d95-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3d95-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d95-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d95-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3d95-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3d95-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b3d95-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b3d95-123">-ServerName</span></span>
<span data-ttu-id="b3d95-124">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="b3d95-124">SQL server name.</span></span>

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

### <span data-ttu-id="b3d95-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d95-125">CommonParameters</span></span>
<span data-ttu-id="b3d95-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d95-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d95-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3d95-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d95-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3d95-128">INPUTS</span></span>

### <span data-ttu-id="b3d95-129">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b3d95-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b3d95-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3d95-130">OUTPUTS</span></span>

### <span data-ttu-id="b3d95-131">Microsoft. Azure. Commands. SQL. dataklasyfikacyjn. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b3d95-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="b3d95-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3d95-132">NOTES</span></span>

## <span data-ttu-id="b3d95-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3d95-133">RELATED LINKS</span></span>

[<span data-ttu-id="b3d95-134">Więcej informacji na temat wykrywania i klasyfikacji danych w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b3d95-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
