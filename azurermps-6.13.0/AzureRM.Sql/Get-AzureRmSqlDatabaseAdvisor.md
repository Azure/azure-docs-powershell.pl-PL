---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
ms.openlocfilehash: 853702ab34a6a9dab7e90f2335f99deb7155a837
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548540"
---
# <span data-ttu-id="99615-101">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="99615-101">Get-AzureRmSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="99615-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99615-102">SYNOPSIS</span></span>
<span data-ttu-id="99615-103">Pobiera co najmniej jeden klasyfikator dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="99615-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99615-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99615-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99615-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99615-105">DESCRIPTION</span></span>
<span data-ttu-id="99615-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseAdvisor** pobiera co najmniej jeden klasyfikator bazy danych SQL Azure dla bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="99615-106">The **Get-AzureRmSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="99615-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99615-107">EXAMPLES</span></span>

### <span data-ttu-id="99615-108">Przykład 1. Lista wszystkich klasyfikatorów dla określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="99615-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
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

<span data-ttu-id="99615-109">To polecenie pobiera listę wszystkich doradców bazy danych o nazwie WIRunner, które należą do serwera o nazwie Wi-Runner-Australia-wschód.</span><span class="sxs-lookup"><span data-stu-id="99615-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="99615-110">Przykład 2: uzyskiwanie jednego klasyfikatora dla określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="99615-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

<span data-ttu-id="99615-111">To polecenie umożliwia wyświetlenie klasyfikatora o nazwie Moja indeks dla bazy danych o nazwie WIRunner.</span><span class="sxs-lookup"><span data-stu-id="99615-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="99615-112">Przykład 3: wyświetlanie wszystkich doradców z zalecanymi działaniami zawartymi w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="99615-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
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

<span data-ttu-id="99615-113">To polecenie uzyskuje Wszystkie klasyfikatory dla bazy danych o nazwie "WIRunner" z zalecanymi akcjami zawartymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="99615-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="99615-114">Ponieważ w poleceniu jest używany parametr *ExpandRecommendedActions* , polecenie cmdlet umożliwia pobieranie zalecanych akcji wraz z odpowiedzią.</span><span class="sxs-lookup"><span data-stu-id="99615-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="99615-115">Przykład 4: uzyskiwanie jednego klasyfikatora z zalecanymi akcjami zawartymi w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="99615-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="99615-116">To polecenie pobiera klasyfikator o nazwie Moja indeks z bazy danych o nazwie WIRunner z zalecanymi akcjami zawartymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="99615-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="99615-117">Ponieważ w poleceniu jest używany parametr *ExpandRecommendedActions* , polecenie cmdlet umożliwia pobieranie zalecanych akcji wraz z odpowiedzią.</span><span class="sxs-lookup"><span data-stu-id="99615-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

## <span data-ttu-id="99615-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99615-118">PARAMETERS</span></span>

### <span data-ttu-id="99615-119">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="99615-119">-AdvisorName</span></span>
<span data-ttu-id="99615-120">Określa nazwę klasyfikatora, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99615-120">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="99615-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="99615-121">-DatabaseName</span></span>
<span data-ttu-id="99615-122">Określa nazwę bazy danych, dla której to polecenie cmdlet żąda klasyfikatora.</span><span class="sxs-lookup"><span data-stu-id="99615-122">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="99615-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99615-123">-DefaultProfile</span></span>
<span data-ttu-id="99615-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="99615-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99615-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="99615-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="99615-126">Wskazuje, że polecenie cmdlet umożliwia pobieranie zalecanych akcji wraz z odpowiedzią.</span><span class="sxs-lookup"><span data-stu-id="99615-126">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="99615-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99615-127">-ResourceGroupName</span></span>
<span data-ttu-id="99615-128">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="99615-128">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="99615-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="99615-129">-ServerName</span></span>
<span data-ttu-id="99615-130">Określa nazwę serwera, który zawiera bazę danych.</span><span class="sxs-lookup"><span data-stu-id="99615-130">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="99615-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99615-131">CommonParameters</span></span>
<span data-ttu-id="99615-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99615-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99615-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99615-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99615-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99615-134">INPUTS</span></span>

### <span data-ttu-id="99615-135">System. String</span><span class="sxs-lookup"><span data-stu-id="99615-135">System.String</span></span>

### <span data-ttu-id="99615-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99615-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99615-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99615-137">OUTPUTS</span></span>

### <span data-ttu-id="99615-138">Microsoft. Azure. Commands. SQL. Advisor. model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="99615-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="99615-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99615-139">NOTES</span></span>
* <span data-ttu-id="99615-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL, Doradca</span><span class="sxs-lookup"><span data-stu-id="99615-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="99615-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99615-141">RELATED LINKS</span></span>

[<span data-ttu-id="99615-142">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="99615-142">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="99615-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="99615-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="99615-144">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="99615-144">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="99615-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="99615-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="99615-146">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="99615-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
