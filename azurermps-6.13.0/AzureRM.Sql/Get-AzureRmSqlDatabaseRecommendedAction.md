---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EF6C862B-A89C-48AB-A590-92CFA387305F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaserecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRecommendedAction.md
ms.openlocfilehash: cf0f8c3be01f5b3f48eea940bd733d6dd7cc1c1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526029"
---
# <span data-ttu-id="fbaff-101">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="fbaff-101">Get-AzureRmSqlDatabaseRecommendedAction</span></span>

## <span data-ttu-id="fbaff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbaff-102">SYNOPSIS</span></span>
<span data-ttu-id="fbaff-103">Umożliwia wykonanie jednej lub większej liczby zalecanych akcji dla klasyfikatora bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="fbaff-103">Gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbaff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbaff-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbaff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbaff-105">DESCRIPTION</span></span>
<span data-ttu-id="fbaff-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseRecommendedAction** umożliwia wykonanie jednej lub większej liczby zalecanych akcji dla klasyfikatora bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="fbaff-106">The **Get-AzureRmSqlDatabaseRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="fbaff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbaff-107">EXAMPLES</span></span>

### <span data-ttu-id="fbaff-108">Przykład 1: wyświetlanie wszystkich zalecanych akcji dla klasyfikatora</span><span class="sxs-lookup"><span data-stu-id="fbaff-108">Example 1: List all the recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM

DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.236046_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.236046]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {SpaceChange}
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.239359_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.239359]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : PT10S
RevertActionInitiatedBy    : System
RevertActionInitiatedTime  : 4/21/2016 3:24:47 PM
RevertActionStartTime      : 4/21/2016 3:24:47 PM
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="fbaff-109">To polecenie powoduje wyświetlenie listy wszystkich zalecanych akcji klasyfikatora o nazwie Moja indeks dostępnego dla bazy danych o nazwie Wi-Runner-Australia-wschód.</span><span class="sxs-lookup"><span data-stu-id="fbaff-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the database named wi-runner-australia-east.</span></span>

### <span data-ttu-id="fbaff-110">Przykład 2: Uzyskaj jedną zalecaną akcję dla klasyfikatora</span><span class="sxs-lookup"><span data-stu-id="fbaff-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="fbaff-111">To polecenie pobiera zalecaną akcję o nazwie IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 dla klasyfikatora o nazwie Moja indeks.</span><span class="sxs-lookup"><span data-stu-id="fbaff-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 for the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="fbaff-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbaff-112">PARAMETERS</span></span>

### <span data-ttu-id="fbaff-113">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="fbaff-113">-AdvisorName</span></span>
<span data-ttu-id="fbaff-114">Określa nazwę klasyfikatora, dla którego to polecenie cmdlet żąda zalecanych akcji.</span><span class="sxs-lookup"><span data-stu-id="fbaff-114">Specifies the name of the Advisor for which this cmdlet requests recommended actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaff-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbaff-115">-DatabaseName</span></span>
<span data-ttu-id="fbaff-116">Określa nazwę bazy danych, dla której to polecenie cmdlet żąda zalecanych akcji.</span><span class="sxs-lookup"><span data-stu-id="fbaff-116">Specifies the name of the database for which this cmdlet requests recommended actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbaff-117">-DefaultProfile</span></span>
<span data-ttu-id="fbaff-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fbaff-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbaff-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="fbaff-119">-RecommendedActionName</span></span>
<span data-ttu-id="fbaff-120">Określa nazwę zalecanej akcji, która ma być pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbaff-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaff-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbaff-121">-ResourceGroupName</span></span>
<span data-ttu-id="fbaff-122">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="fbaff-122">Specifies name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaff-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fbaff-123">-ServerName</span></span>
<span data-ttu-id="fbaff-124">Określa nazwę serwera, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="fbaff-124">Specifies the name of the server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbaff-125">CommonParameters</span></span>
<span data-ttu-id="fbaff-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbaff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbaff-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbaff-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbaff-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbaff-128">INPUTS</span></span>

### <span data-ttu-id="fbaff-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fbaff-129">System.String</span></span>

## <span data-ttu-id="fbaff-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbaff-130">OUTPUTS</span></span>

### <span data-ttu-id="fbaff-131">Microsoft. Azure. Commands. SQL. RecommendedAction. model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="fbaff-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="fbaff-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbaff-132">NOTES</span></span>
* <span data-ttu-id="fbaff-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="fbaff-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="fbaff-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbaff-134">RELATED LINKS</span></span>

[<span data-ttu-id="fbaff-135">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="fbaff-135">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="fbaff-136">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="fbaff-136">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="fbaff-137">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="fbaff-137">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="fbaff-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fbaff-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)