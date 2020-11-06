---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolAdvisor.md
ms.openlocfilehash: 3bb8292c872c02c5d6b092e5e721b15eab24e493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547904"
---
# <span data-ttu-id="8c25f-101">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="8c25f-101">Get-AzureRmSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="8c25f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c25f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c25f-103">Pobiera jeden lub więcej doradców dla puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8c25f-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c25f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c25f-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c25f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8c25f-105">DESCRIPTION</span></span>
<span data-ttu-id="8c25f-106">Polecenie cmdlet **Get-AzureRmSqlElasticPoolAdvisor** pobiera co najmniej jeden Doradca puli elastycznej SQL platformy Azure dla puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8c25f-106">The **Get-AzureRmSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="8c25f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c25f-107">EXAMPLES</span></span>

### <span data-ttu-id="8c25f-108">Przykład 1: wyświetlanie wszystkich doradców dla określonej puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="8c25f-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -PoolName "WIRunnerPool"
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

<span data-ttu-id="8c25f-109">Polecenie pobiera listę wszystkich doradców dla puli elastycznej o nazwie WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="8c25f-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="8c25f-110">Przykład 2: uzyskiwanie jednego klasyfikatora dla określonej puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="8c25f-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
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

<span data-ttu-id="8c25f-111">To polecenie pobiera klasyfikator o nazwie Moja indeks dla puli elastycznej o nazwie WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="8c25f-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="8c25f-112">Przykład 3: wyświetlanie wszystkich doradców z zalecanymi działaniami zawartymi w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="8c25f-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
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

<span data-ttu-id="8c25f-113">To polecenie pobiera wszystkich doradców do puli elastycznej z zalecanymi działaniami zawartymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="8c25f-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="8c25f-114">Przykład 4: uzyskiwanie jednego klasyfikatora z zalecanymi akcjami zawartymi w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="8c25f-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="8c25f-115">To polecenie pobiera klasyfikator o nazwie Moja indeks z serwera o nazwie Wi-Runner-Australia-wschód z zalecanymi działaniami zawartymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="8c25f-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

## <span data-ttu-id="8c25f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c25f-116">PARAMETERS</span></span>

### <span data-ttu-id="8c25f-117">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="8c25f-117">-AdvisorName</span></span>
<span data-ttu-id="8c25f-118">Określa nazwę klasyfikatora, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c25f-118">Specifies the name of the Advisor that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c25f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c25f-119">-DefaultProfile</span></span>
<span data-ttu-id="8c25f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8c25f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c25f-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8c25f-121">-ElasticPoolName</span></span>
<span data-ttu-id="8c25f-122">Określa nazwę puli elastycznej, dla której to polecenie cmdlet żąda klasyfikatora.</span><span class="sxs-lookup"><span data-stu-id="8c25f-122">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c25f-123">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="8c25f-123">-ExpandRecommendedActions</span></span>
<span data-ttu-id="8c25f-124">Wskazuje, że polecenie cmdlet zawiera zalecane działania klasyfikatora w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="8c25f-124">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c25f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c25f-125">-ResourceGroupName</span></span>
<span data-ttu-id="8c25f-126">Określa nazwę grupy zasobów serwera, która zawiera tę pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="8c25f-126">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c25f-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8c25f-127">-ServerName</span></span>
<span data-ttu-id="8c25f-128">Określa nazwę serwera, na którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="8c25f-128">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c25f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c25f-129">CommonParameters</span></span>
<span data-ttu-id="8c25f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c25f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c25f-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c25f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c25f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c25f-132">INPUTS</span></span>

### <span data-ttu-id="8c25f-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8c25f-133">None</span></span>
<span data-ttu-id="8c25f-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8c25f-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c25f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c25f-135">OUTPUTS</span></span>

### <span data-ttu-id="8c25f-136">Microsoft. Azure. Commands. SQL. Advisor. model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="8c25f-136">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="8c25f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c25f-137">NOTES</span></span>
* <span data-ttu-id="8c25f-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Doradca</span><span class="sxs-lookup"><span data-stu-id="8c25f-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="8c25f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c25f-139">RELATED LINKS</span></span>

[<span data-ttu-id="8c25f-140">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="8c25f-140">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="8c25f-141">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="8c25f-141">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="8c25f-142">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="8c25f-142">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="8c25f-143">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8c25f-143">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="8c25f-144">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="8c25f-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
