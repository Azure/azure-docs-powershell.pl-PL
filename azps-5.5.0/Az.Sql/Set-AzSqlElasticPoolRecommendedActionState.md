---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176747"
---
# <span data-ttu-id="93e24-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="93e24-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="93e24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e24-102">SYNOPSIS</span></span>
<span data-ttu-id="93e24-103">Aktualizuje stan zalecanej czynności w puli elastycznej języka SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="93e24-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="93e24-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93e24-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e24-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="93e24-105">DESCRIPTION</span></span>
<span data-ttu-id="93e24-106">Polecenie **cmdlet Set-AzSqlElasticPoolRecomctionActionState** aktualizuje stan zalecanej akcji Puli elastycznej języka AZURE SQL.</span><span class="sxs-lookup"><span data-stu-id="93e24-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="93e24-107">To polecenie cmdlet powoduje zastosowanie zalecanej akcji, przywrócenie lub odrzucenie w zależności od nowego stanu.</span><span class="sxs-lookup"><span data-stu-id="93e24-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="93e24-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93e24-108">EXAMPLES</span></span>

### <span data-ttu-id="93e24-109">Przykład 1. Aktualizowanie stanu zalecanej akcji do stanu Oczekujące</span><span class="sxs-lookup"><span data-stu-id="93e24-109">Example 1: Update the state of a recommended action to Pending</span></span>
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

<span data-ttu-id="93e24-110">To polecenie aktualizuje stan elastycznej puli zalecanej akcji o nazwie IR_ \[ test_schema \] _ \[ test_table_0,0361551 _6C7AE8CC9C87E7FD5893 \] wartość Oczekiwanie.</span><span class="sxs-lookup"><span data-stu-id="93e24-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="93e24-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93e24-111">PARAMETERS</span></span>

### <span data-ttu-id="93e24-112">- AdvisorName</span><span class="sxs-lookup"><span data-stu-id="93e24-112">-AdvisorName</span></span>
<span data-ttu-id="93e24-113">Określa nazwę doradcy, do którego należy ta zalecana akcja.</span><span class="sxs-lookup"><span data-stu-id="93e24-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="93e24-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e24-114">-DefaultProfile</span></span>
<span data-ttu-id="93e24-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="93e24-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93e24-116">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="93e24-116">-ElasticPoolName</span></span>
<span data-ttu-id="93e24-117">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="93e24-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="93e24-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="93e24-118">-RecommendedActionName</span></span>
<span data-ttu-id="93e24-119">Określa nazwę zalecanej akcji, dla której to polecenie cmdlet aktualizuje stan.</span><span class="sxs-lookup"><span data-stu-id="93e24-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="93e24-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e24-120">-ResourceGroupName</span></span>
<span data-ttu-id="93e24-121">Określa nazwę grupy zasobów serwera zawierającej tę elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="93e24-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="93e24-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93e24-122">-ServerName</span></span>
<span data-ttu-id="93e24-123">Określa nazwę serwera, w którym znajduje się elastyczna pula.</span><span class="sxs-lookup"><span data-stu-id="93e24-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="93e24-124">— województwo</span><span class="sxs-lookup"><span data-stu-id="93e24-124">-State</span></span>
<span data-ttu-id="93e24-125">Określa wartość, dla której to polecenie cmdlet aktualizuje stan zalecanej akcji.</span><span class="sxs-lookup"><span data-stu-id="93e24-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="93e24-126">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="93e24-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93e24-127">Aktywny</span><span class="sxs-lookup"><span data-stu-id="93e24-127">Active</span></span>
- <span data-ttu-id="93e24-128">Oczekiwanie</span><span class="sxs-lookup"><span data-stu-id="93e24-128">Pending</span></span>
- <span data-ttu-id="93e24-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="93e24-129">PendingRevert</span></span>
- <span data-ttu-id="93e24-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="93e24-130">RevertCancelled</span></span>
- <span data-ttu-id="93e24-131">Ignorowane</span><span class="sxs-lookup"><span data-stu-id="93e24-131">Ignored</span></span>
- <span data-ttu-id="93e24-132">Rozwiązano</span><span class="sxs-lookup"><span data-stu-id="93e24-132">Resolved</span></span>

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

### <span data-ttu-id="93e24-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93e24-133">-Confirm</span></span>
<span data-ttu-id="93e24-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="93e24-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e24-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e24-135">-WhatIf</span></span>
<span data-ttu-id="93e24-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93e24-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e24-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="93e24-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e24-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e24-138">CommonParameters</span></span>
<span data-ttu-id="93e24-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e24-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e24-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93e24-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e24-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93e24-141">INPUTS</span></span>

### <span data-ttu-id="93e24-142">System.String</span><span class="sxs-lookup"><span data-stu-id="93e24-142">System.String</span></span>

### <span data-ttu-id="93e24-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="93e24-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="93e24-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93e24-144">OUTPUTS</span></span>

### <span data-ttu-id="93e24-145">Microsoft.Azure.Commands.sql.RecommendedAction.Model.AzureSqlElasticPoolRecomctionActionModel</span><span class="sxs-lookup"><span data-stu-id="93e24-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="93e24-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93e24-146">NOTES</span></span>
* <span data-ttu-id="93e24-147">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql,basepool, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="93e24-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="93e24-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93e24-148">RELATED LINKS</span></span>

[<span data-ttu-id="93e24-149">Get-AzSqlElasticPoolRecomctionAction</span><span class="sxs-lookup"><span data-stu-id="93e24-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="93e24-150">Set-AzSqlDatabaseRecomctionActionState</span><span class="sxs-lookup"><span data-stu-id="93e24-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="93e24-151">Set-AzSqlServerRecomctionActionState</span><span class="sxs-lookup"><span data-stu-id="93e24-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="93e24-152">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="93e24-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
