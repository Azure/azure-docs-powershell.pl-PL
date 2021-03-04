---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
ms.openlocfilehash: 9c9a6b2b95f5126ecdc214db2227c46b01c5725c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999537"
---
# <span data-ttu-id="fbdbf-101">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="fbdbf-101">Get-AzSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="fbdbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbdbf-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdbf-103">Otrzymuje co najmniej jednego doradcę dla puli elastycznej języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="fbdbf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fbdbf-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbdbf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fbdbf-105">DESCRIPTION</span></span>
<span data-ttu-id="fbdbf-106">Polecenie **cmdlet Get-AzSqlElasticPoolAdvisor** pobiera co najmniej jednego doradcę puli elastycznej języka Azure SQL dla puli elastycznej języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-106">The **Get-AzSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="fbdbf-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fbdbf-107">EXAMPLES</span></span>

### <span data-ttu-id="fbdbf-108">Przykład 1. Lista wszystkich doradców dla określonej puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="fbdbf-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool"
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="fbdbf-109">To polecenie wyświetla listę wszystkich doradców puli elastycznej o nazwie WIPoolPool.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="fbdbf-110">Przykład 2. Uzyskiwanie pojedynczego doradcy dla określonej puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="fbdbf-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="fbdbf-111">To polecenie pobiera doradcę o nazwie CreateIndex dla puli elastycznej o nazwie WIPool.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="fbdbf-112">Przykład 3. Lista wszystkich doradców z ich zalecanymi działaniami uwzględnionych w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="fbdbf-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="fbdbf-113">To polecenie pobiera wszystkich doradców dla elastycznej puli z ich zalecanymi działaniami uwzględnioną w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="fbdbf-114">Przykład 4. Uzyskiwanie pojedynczego doradcy z zalecanymi działaniami uwzględnionych w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="fbdbf-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="fbdbf-115">To polecenie pobiera doradcę o nazwie CreateIndex z serwera o nazwie wi-biegacz-australia-wschód z zalecanymi akcjami uwzględnionymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="fbdbf-116">Przykład 5. Lista wszystkich doradców dla określonej puli elastycznej przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="fbdbf-116">Example 5: List all the advisors for the specified elastic pool using filtering</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName d*
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="fbdbf-117">To polecenie wyświetla listę wszystkich doradców puli elastycznej o nazwie WIPool, których nazwa rozpoczyna się od litery "d".</span><span class="sxs-lookup"><span data-stu-id="fbdbf-117">The command gets lists all the advisors for the elastic pool named WIRunnerPool that start with the letter "d".</span></span>

## <span data-ttu-id="fbdbf-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbdbf-118">PARAMETERS</span></span>

### <span data-ttu-id="fbdbf-119">- AdvisorName</span><span class="sxs-lookup"><span data-stu-id="fbdbf-119">-AdvisorName</span></span>
<span data-ttu-id="fbdbf-120">Określa nazwę doradcy, do otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-120">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fbdbf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbdbf-121">-DefaultProfile</span></span>
<span data-ttu-id="fbdbf-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fbdbf-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbdbf-123">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="fbdbf-123">-ElasticPoolName</span></span>
<span data-ttu-id="fbdbf-124">Określa nazwę puli elastycznej, dla której to polecenie cmdlet żąda doradcy.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-124">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="fbdbf-125">-ExpandRecomctionActions</span><span class="sxs-lookup"><span data-stu-id="fbdbf-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="fbdbf-126">Wskazuje, że polecenie cmdlet zawiera w odpowiedzi zalecane akcje doradcy.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-126">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="fbdbf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbdbf-127">-ResourceGroupName</span></span>
<span data-ttu-id="fbdbf-128">Określa nazwę grupy zasobów serwera, która zawiera tę elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-128">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="fbdbf-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fbdbf-129">-ServerName</span></span>
<span data-ttu-id="fbdbf-130">Określa nazwę serwera, w którym znajduje się elastyczna pula.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-130">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="fbdbf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdbf-131">CommonParameters</span></span>
<span data-ttu-id="fbdbf-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbdbf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdbf-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbdbf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdbf-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbdbf-134">INPUTS</span></span>

### <span data-ttu-id="fbdbf-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fbdbf-135">System.String</span></span>

### <span data-ttu-id="fbdbf-136">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="fbdbf-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fbdbf-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbdbf-137">OUTPUTS</span></span>

### <span data-ttu-id="fbdbf-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="fbdbf-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="fbdbf-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fbdbf-139">NOTES</span></span>
* <span data-ttu-id="fbdbf-140">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql,pool i mssql, doradca</span><span class="sxs-lookup"><span data-stu-id="fbdbf-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="fbdbf-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbdbf-141">RELATED LINKS</span></span>

[<span data-ttu-id="fbdbf-142">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="fbdbf-142">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="fbdbf-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="fbdbf-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="fbdbf-144">Get-AzSqlElasticPoolRecomctionAction</span><span class="sxs-lookup"><span data-stu-id="fbdbf-144">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="fbdbf-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="fbdbf-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="fbdbf-146">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fbdbf-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
