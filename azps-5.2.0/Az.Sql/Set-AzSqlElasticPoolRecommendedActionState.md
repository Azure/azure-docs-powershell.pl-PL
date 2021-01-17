---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337189"
---
# <span data-ttu-id="fc709-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="fc709-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="fc709-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc709-102">SYNOPSIS</span></span>
<span data-ttu-id="fc709-103">Aktualizuje stan zalecanej akcji puli elastycznej w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fc709-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="fc709-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc709-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc709-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fc709-105">DESCRIPTION</span></span>
<span data-ttu-id="fc709-106">Stan aktualizacji polecenia cmdlet **Set-AzSqlElasticPoolRecommendedActionState** w przypadku zalecanej akcji puli elastycznej w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fc709-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="fc709-107">To polecenie cmdlet powoduje zastosowanie zalecanej akcji, która została przywrócona lub odrzucona na podstawie nowego stanu.</span><span class="sxs-lookup"><span data-stu-id="fc709-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="fc709-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc709-108">EXAMPLES</span></span>

### <span data-ttu-id="fc709-109">Przykład 1: aktualizowanie stanu zalecanej akcji na oczekujące</span><span class="sxs-lookup"><span data-stu-id="fc709-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ElasticPoolName            : WIRunnerPool
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

<span data-ttu-id="fc709-110">To polecenie powoduje zaktualizowanie stanu zalecanej akcji puli elastycznej o nazwie IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 na oczekujące.</span><span class="sxs-lookup"><span data-stu-id="fc709-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="fc709-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc709-111">PARAMETERS</span></span>

### <span data-ttu-id="fc709-112">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="fc709-112">-AdvisorName</span></span>
<span data-ttu-id="fc709-113">Określa nazwę klasyfikatora, do którego należy zalecana akcja.</span><span class="sxs-lookup"><span data-stu-id="fc709-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="fc709-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc709-114">-DefaultProfile</span></span>
<span data-ttu-id="fc709-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fc709-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc709-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fc709-116">-ElasticPoolName</span></span>
<span data-ttu-id="fc709-117">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="fc709-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="fc709-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="fc709-118">-RecommendedActionName</span></span>
<span data-ttu-id="fc709-119">Określa nazwę zalecanej akcji, dla której to polecenie cmdlet aktualizuje stan.</span><span class="sxs-lookup"><span data-stu-id="fc709-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="fc709-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc709-120">-ResourceGroupName</span></span>
<span data-ttu-id="fc709-121">Określa nazwę grupy zasobów serwera, która zawiera tę pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="fc709-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="fc709-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fc709-122">-ServerName</span></span>
<span data-ttu-id="fc709-123">Określa nazwę serwera, na którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="fc709-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="fc709-124">-State</span><span class="sxs-lookup"><span data-stu-id="fc709-124">-State</span></span>
<span data-ttu-id="fc709-125">Określa wartość, na którą to polecenie cmdlet aktualizuje zalecany stan akcji.</span><span class="sxs-lookup"><span data-stu-id="fc709-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="fc709-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fc709-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fc709-127">Active</span><span class="sxs-lookup"><span data-stu-id="fc709-127">Active</span></span>
- <span data-ttu-id="fc709-128">Wybranego</span><span class="sxs-lookup"><span data-stu-id="fc709-128">Pending</span></span>
- <span data-ttu-id="fc709-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="fc709-129">PendingRevert</span></span>
- <span data-ttu-id="fc709-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="fc709-130">RevertCancelled</span></span>
- <span data-ttu-id="fc709-131">Zignorowała</span><span class="sxs-lookup"><span data-stu-id="fc709-131">Ignored</span></span>
- <span data-ttu-id="fc709-132">Rozpoznawania</span><span class="sxs-lookup"><span data-stu-id="fc709-132">Resolved</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc709-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc709-133">-Confirm</span></span>
<span data-ttu-id="fc709-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc709-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc709-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc709-135">-WhatIf</span></span>
<span data-ttu-id="fc709-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc709-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc709-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc709-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc709-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc709-138">CommonParameters</span></span>
<span data-ttu-id="fc709-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc709-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc709-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc709-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc709-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc709-141">INPUTS</span></span>

### <span data-ttu-id="fc709-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fc709-142">System.String</span></span>

### <span data-ttu-id="fc709-143">Microsoft. Azure. Commands. SQL. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="fc709-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="fc709-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc709-144">OUTPUTS</span></span>

### <span data-ttu-id="fc709-145">Microsoft. Azure. Commands. SQL. RecommendedAction. model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="fc709-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="fc709-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc709-146">NOTES</span></span>
* <span data-ttu-id="fc709-147">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Doradca, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="fc709-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="fc709-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc709-148">RELATED LINKS</span></span>

[<span data-ttu-id="fc709-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="fc709-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="fc709-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="fc709-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="fc709-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="fc709-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="fc709-152">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fc709-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
