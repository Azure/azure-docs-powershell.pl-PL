---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: 05bde2ee8a5bbcae941203115c49ff6b9fbc6bae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368613"
---
# <span data-ttu-id="3421f-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="3421f-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="3421f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3421f-102">SYNOPSIS</span></span>
<span data-ttu-id="3421f-103">Pobiera co najmniej jeden klasyfikator dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3421f-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="3421f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3421f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3421f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3421f-105">DESCRIPTION</span></span>
<span data-ttu-id="3421f-106">Polecenie cmdlet **Get-AzSqlDatabaseAdvisor** pobiera co najmniej jeden klasyfikator bazy danych SQL Azure dla bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3421f-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="3421f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3421f-107">EXAMPLES</span></span>

### <span data-ttu-id="3421f-108">Przykład 1. Lista wszystkich klasyfikatorów dla określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="3421f-108">Example 1: List all the advisors for the specified database</span></span>
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

<span data-ttu-id="3421f-109">To polecenie pobiera listę wszystkich doradców bazy danych o nazwie WIRunner, które należą do serwera o nazwie Wi-Runner-Australia-wschód.</span><span class="sxs-lookup"><span data-stu-id="3421f-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="3421f-110">Przykład 2: uzyskiwanie jednego klasyfikatora dla określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="3421f-110">Example 2: Get a single advisor for the specified database</span></span>
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

<span data-ttu-id="3421f-111">To polecenie umożliwia wyświetlenie klasyfikatora o nazwie Moja indeks dla bazy danych o nazwie WIRunner.</span><span class="sxs-lookup"><span data-stu-id="3421f-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="3421f-112">Przykład 3: wyświetlanie wszystkich doradców z zalecanymi działaniami zawartymi w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="3421f-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="3421f-113">To polecenie uzyskuje Wszystkie klasyfikatory dla bazy danych o nazwie "WIRunner" z zalecanymi akcjami zawartymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="3421f-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="3421f-114">Ponieważ w poleceniu jest używany parametr *ExpandRecommendedActions* , polecenie cmdlet umożliwia pobieranie zalecanych akcji wraz z odpowiedzią.</span><span class="sxs-lookup"><span data-stu-id="3421f-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="3421f-115">Przykład 4: uzyskiwanie jednego klasyfikatora z zalecanymi akcjami zawartymi w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="3421f-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="3421f-116">To polecenie pobiera klasyfikator o nazwie Moja indeks z bazy danych o nazwie WIRunner z zalecanymi akcjami zawartymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="3421f-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="3421f-117">Ponieważ w poleceniu jest używany parametr *ExpandRecommendedActions* , polecenie cmdlet umożliwia pobieranie zalecanych akcji wraz z odpowiedzią.</span><span class="sxs-lookup"><span data-stu-id="3421f-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="3421f-118">Przykład 5: wyświetlanie wszystkich klasyfikatorów dla określonej bazy danych przy użyciu funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="3421f-118">Example 5: List all the advisors for the specified database using filtering</span></span>
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

<span data-ttu-id="3421f-119">To polecenie pobiera listę wszystkich doradców bazy danych o nazwie WIRunner, które należą do serwera o nazwie Wi-Runner-Australia-wschód, i zaczynają się literą "d".</span><span class="sxs-lookup"><span data-stu-id="3421f-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="3421f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3421f-120">PARAMETERS</span></span>

### <span data-ttu-id="3421f-121">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="3421f-121">-AdvisorName</span></span>
<span data-ttu-id="3421f-122">Określa nazwę klasyfikatora, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3421f-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3421f-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3421f-123">-DatabaseName</span></span>
<span data-ttu-id="3421f-124">Określa nazwę bazy danych, dla której to polecenie cmdlet żąda klasyfikatora.</span><span class="sxs-lookup"><span data-stu-id="3421f-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="3421f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3421f-125">-DefaultProfile</span></span>
<span data-ttu-id="3421f-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3421f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3421f-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="3421f-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="3421f-128">Wskazuje, że polecenie cmdlet umożliwia pobieranie zalecanych akcji wraz z odpowiedzią.</span><span class="sxs-lookup"><span data-stu-id="3421f-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="3421f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3421f-129">-ResourceGroupName</span></span>
<span data-ttu-id="3421f-130">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="3421f-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="3421f-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3421f-131">-ServerName</span></span>
<span data-ttu-id="3421f-132">Określa nazwę serwera, który zawiera bazę danych.</span><span class="sxs-lookup"><span data-stu-id="3421f-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="3421f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3421f-133">CommonParameters</span></span>
<span data-ttu-id="3421f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3421f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3421f-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3421f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3421f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3421f-136">INPUTS</span></span>

### <span data-ttu-id="3421f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3421f-137">System.String</span></span>

### <span data-ttu-id="3421f-138">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3421f-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3421f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3421f-139">OUTPUTS</span></span>

### <span data-ttu-id="3421f-140">Microsoft. Azure. Commands. SQL. Advisor. model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="3421f-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="3421f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3421f-141">NOTES</span></span>
* <span data-ttu-id="3421f-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL, Doradca</span><span class="sxs-lookup"><span data-stu-id="3421f-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="3421f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3421f-143">RELATED LINKS</span></span>

[<span data-ttu-id="3421f-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="3421f-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="3421f-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="3421f-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="3421f-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="3421f-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="3421f-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3421f-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="3421f-148">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3421f-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
