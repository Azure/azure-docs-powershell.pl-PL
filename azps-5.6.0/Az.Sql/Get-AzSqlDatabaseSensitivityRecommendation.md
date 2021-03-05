---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: de5aa5f3347c7277c54d41de9085426b430f167c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014730"
---
# <span data-ttu-id="743b4-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="743b4-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="743b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="743b4-102">SYNOPSIS</span></span>
<span data-ttu-id="743b4-103">Pobiera zalecane typy informacji i etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="743b4-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="743b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="743b4-104">SYNTAX</span></span>

### <span data-ttu-id="743b4-105">DatabaseObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="743b4-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="743b4-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="743b4-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="743b4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="743b4-107">DESCRIPTION</span></span>
<span data-ttu-id="743b4-108">Polecenie Get-AzSqlDatabaseSensitivityRecommendation zwraca zalecane typy informacji i etykiety wrażliwości kolumn w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="743b4-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="743b4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="743b4-109">EXAMPLES</span></span>

### <span data-ttu-id="743b4-110">Przykład 1. Uzyskaj zalecane typy informacji i etykiety wrażliwości bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="743b4-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
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

### <span data-ttu-id="743b4-111">Przykład 2. Uzyskaj zalecane typy informacji i etykiety wrażliwości bazy danych Azure SQL przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="743b4-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
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

## <span data-ttu-id="743b4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="743b4-112">PARAMETERS</span></span>

### <span data-ttu-id="743b4-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="743b4-113">-AsJob</span></span>
<span data-ttu-id="743b4-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="743b4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="743b4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="743b4-115">-DatabaseName</span></span>
<span data-ttu-id="743b4-116">Nazwa bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="743b4-116">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="743b4-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="743b4-117">-DatabaseObject</span></span>
<span data-ttu-id="743b4-118">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="743b4-118">The SQL database object.</span></span>

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

### <span data-ttu-id="743b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743b4-119">-DefaultProfile</span></span>
<span data-ttu-id="743b4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="743b4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="743b4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743b4-121">-ResourceGroupName</span></span>
<span data-ttu-id="743b4-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="743b4-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="743b4-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="743b4-123">-ServerName</span></span>
<span data-ttu-id="743b4-124">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="743b4-124">SQL server name.</span></span>

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

### <span data-ttu-id="743b4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743b4-125">CommonParameters</span></span>
<span data-ttu-id="743b4-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743b4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743b4-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="743b4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743b4-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="743b4-128">INPUTS</span></span>

### <span data-ttu-id="743b4-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="743b4-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="743b4-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="743b4-130">OUTPUTS</span></span>

### <span data-ttu-id="743b4-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="743b4-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="743b4-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="743b4-132">NOTES</span></span>

## <span data-ttu-id="743b4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="743b4-133">RELATED LINKS</span></span>

[<span data-ttu-id="743b4-134">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="743b4-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
