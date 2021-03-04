---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: d946b6b324247a46760f762c4631419b6c6aac59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967546"
---
# <span data-ttu-id="31df1-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="31df1-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="31df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31df1-102">SYNOPSIS</span></span>
<span data-ttu-id="31df1-103">Otrzymuje co najmniej jednego doradcę w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="31df1-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="31df1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="31df1-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31df1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="31df1-105">DESCRIPTION</span></span>
<span data-ttu-id="31df1-106">Polecenie **cmdlet Get-AzSqlDatabaseAdvisor** pobiera co najmniej jednego doradcę usługi Azure SQL Database Database dla usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="31df1-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="31df1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="31df1-107">EXAMPLES</span></span>

### <span data-ttu-id="31df1-108">Przykład 1. Lista wszystkich doradców w określonej bazie danych</span><span class="sxs-lookup"><span data-stu-id="31df1-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="31df1-109">To polecenie pobiera listę wszystkich doradców bazy danych o nazwie WIRunner, który należy do serwera o nazwie wi-sprinter-australia-east.</span><span class="sxs-lookup"><span data-stu-id="31df1-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="31df1-110">Przykład 2. Uzyskiwanie pojedynczego doradcy dla określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="31df1-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="31df1-111">To polecenie pobiera doradcę o nazwie CreateIndex dla bazy danych o nazwie WIRunner.</span><span class="sxs-lookup"><span data-stu-id="31df1-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="31df1-112">Przykład 3. Lista wszystkich doradców z ich zalecanymi działaniami uwzględnionych w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="31df1-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="31df1-113">To polecenie pobiera wszystkich doradców bazy danych o nazwie "WIRunner" z ich zalecanymi działaniami uwzględnionymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="31df1-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="31df1-114">Ponieważ to polecenie używa *parametru ExpandRecomctions,* polecenie cmdlet pobiera zalecane akcje wraz z odpowiedzią.</span><span class="sxs-lookup"><span data-stu-id="31df1-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="31df1-115">Przykład 4. Uzyskiwanie pojedynczego doradcy z zalecanymi działaniami uwzględnionych w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="31df1-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="31df1-116">To polecenie pobiera doradcę o nazwie CreateIndex z bazy danych o nazwie WIRunner z zalecanymi akcjami uwzględnionymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="31df1-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="31df1-117">Ponieważ to polecenie używa *parametru ExpandRecomctions,* polecenie cmdlet pobiera zalecane akcje wraz z odpowiedzią.</span><span class="sxs-lookup"><span data-stu-id="31df1-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="31df1-118">Przykład 5. Lista wszystkich doradców w określonej bazie danych przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="31df1-118">Example 5: List all the advisors for the specified database using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName d*
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
```

<span data-ttu-id="31df1-119">To polecenie pobiera listę wszystkich doradców bazy danych o nazwie WIRunner, który należy do serwera o nazwie wi-biegacz-australia-wschód i zaczyna się od litery "d".</span><span class="sxs-lookup"><span data-stu-id="31df1-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="31df1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31df1-120">PARAMETERS</span></span>

### <span data-ttu-id="31df1-121">- AdvisorName</span><span class="sxs-lookup"><span data-stu-id="31df1-121">-AdvisorName</span></span>
<span data-ttu-id="31df1-122">Określa nazwę doradcy, do otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31df1-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="31df1-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="31df1-123">-DatabaseName</span></span>
<span data-ttu-id="31df1-124">Określa nazwę bazy danych, dla której to polecenie cmdlet żąda doradcy.</span><span class="sxs-lookup"><span data-stu-id="31df1-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="31df1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31df1-125">-DefaultProfile</span></span>
<span data-ttu-id="31df1-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="31df1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31df1-127">-ExpandRecomctionActions</span><span class="sxs-lookup"><span data-stu-id="31df1-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="31df1-128">Wskazuje, że to polecenie cmdlet pobiera zalecane akcje wraz z odpowiedzią.</span><span class="sxs-lookup"><span data-stu-id="31df1-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31df1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31df1-129">-ResourceGroupName</span></span>
<span data-ttu-id="31df1-130">Określa nazwę grupy zasobów serwera zawierającego tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="31df1-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="31df1-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="31df1-131">-ServerName</span></span>
<span data-ttu-id="31df1-132">Określa nazwę serwera zawierającego bazę danych.</span><span class="sxs-lookup"><span data-stu-id="31df1-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="31df1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31df1-133">CommonParameters</span></span>
<span data-ttu-id="31df1-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31df1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31df1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31df1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31df1-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31df1-136">INPUTS</span></span>

### <span data-ttu-id="31df1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="31df1-137">System.String</span></span>

### <span data-ttu-id="31df1-138">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="31df1-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31df1-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31df1-139">OUTPUTS</span></span>

### <span data-ttu-id="31df1-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="31df1-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="31df1-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="31df1-141">NOTES</span></span>
* <span data-ttu-id="31df1-142">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="31df1-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="31df1-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31df1-143">RELATED LINKS</span></span>

[<span data-ttu-id="31df1-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="31df1-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="31df1-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="31df1-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="31df1-146">Get-AzSqlDatabaseRecomctionAction</span><span class="sxs-lookup"><span data-stu-id="31df1-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="31df1-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="31df1-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="31df1-148">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="31df1-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
