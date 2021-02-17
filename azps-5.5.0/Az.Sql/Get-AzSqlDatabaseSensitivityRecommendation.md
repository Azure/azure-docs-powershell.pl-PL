---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f002dca1c91ada808acc81108d3f06e9376a8b3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191122"
---
# <span data-ttu-id="64a26-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="64a26-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="64a26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64a26-102">SYNOPSIS</span></span>
<span data-ttu-id="64a26-103">Pobiera zalecane typy informacji i etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="64a26-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="64a26-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64a26-104">SYNTAX</span></span>

### <span data-ttu-id="64a26-105">DatabaseObjectParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="64a26-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64a26-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="64a26-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64a26-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="64a26-107">DESCRIPTION</span></span>
<span data-ttu-id="64a26-108">Polecenie Get-AzSqlDatabaseSensitivityRecommendation zwraca zalecane typy informacji i etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="64a26-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="64a26-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64a26-109">EXAMPLES</span></span>

### <span data-ttu-id="64a26-110">Przykład 1. Uzyskaj zalecane typy informacji i etykiety wrażliwości bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="64a26-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
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

### <span data-ttu-id="64a26-111">Przykład 2. Uzyskaj zalecane typy informacji i etykiety wrażliwości bazy danych Azure SQL przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="64a26-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
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

## <span data-ttu-id="64a26-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64a26-112">PARAMETERS</span></span>

### <span data-ttu-id="64a26-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="64a26-113">-AsJob</span></span>
<span data-ttu-id="64a26-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="64a26-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64a26-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="64a26-115">-DatabaseName</span></span>
<span data-ttu-id="64a26-116">Nazwa bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="64a26-116">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="64a26-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="64a26-117">-DatabaseObject</span></span>
<span data-ttu-id="64a26-118">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="64a26-118">The SQL database object.</span></span>

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

### <span data-ttu-id="64a26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a26-119">-DefaultProfile</span></span>
<span data-ttu-id="64a26-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="64a26-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a26-121">-ResourceGroupName</span></span>
<span data-ttu-id="64a26-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64a26-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="64a26-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="64a26-123">-ServerName</span></span>
<span data-ttu-id="64a26-124">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="64a26-124">SQL server name.</span></span>

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

### <span data-ttu-id="64a26-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a26-125">CommonParameters</span></span>
<span data-ttu-id="64a26-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a26-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a26-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64a26-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a26-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64a26-128">INPUTS</span></span>

### <span data-ttu-id="64a26-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="64a26-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="64a26-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64a26-130">OUTPUTS</span></span>

### <span data-ttu-id="64a26-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="64a26-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="64a26-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64a26-132">NOTES</span></span>

## <span data-ttu-id="64a26-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64a26-133">RELATED LINKS</span></span>

[<span data-ttu-id="64a26-134">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="64a26-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
