---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 5589907f29790d34ab6cc96432f6367894143838
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959322"
---
# <span data-ttu-id="2b005-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="2b005-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="2b005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b005-102">SYNOPSIS</span></span>
<span data-ttu-id="2b005-103">Aktualizuje stan zalecanej akcji w programie Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2b005-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="2b005-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2b005-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b005-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2b005-105">DESCRIPTION</span></span>
<span data-ttu-id="2b005-106">Polecenie **cmdlet Set-AzSqlServerRecomctionState** aktualizuje stan zalecanej akcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2b005-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="2b005-107">To polecenie cmdlet stosuje, przywraca lub odrzuca zalecane działanie na podstawie nowego stanu.</span><span class="sxs-lookup"><span data-stu-id="2b005-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="2b005-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2b005-108">EXAMPLES</span></span>

### <span data-ttu-id="2b005-109">Przykład1. Aktualizowanie stanu określonej zalecanej akcji do stanu Oczekujące</span><span class="sxs-lookup"><span data-stu-id="2b005-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="2b005-110">Aktualizacja zalecanej akcji dotyczącej stanu serwera o nazwie "IR_ \[ test_schema \] _ \[ test_table_0,0361551 _6C7AE8CC9C87E7FD5893" na \] wartość "Oczekujące"</span><span class="sxs-lookup"><span data-stu-id="2b005-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="2b005-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b005-111">PARAMETERS</span></span>

### <span data-ttu-id="2b005-112">- AdvisorName</span><span class="sxs-lookup"><span data-stu-id="2b005-112">-AdvisorName</span></span>
<span data-ttu-id="2b005-113">Określa nazwę doradcy zawierającego zalecaną akcję.</span><span class="sxs-lookup"><span data-stu-id="2b005-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="2b005-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b005-114">-DefaultProfile</span></span>
<span data-ttu-id="2b005-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2b005-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b005-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="2b005-116">-RecommendedActionName</span></span>
<span data-ttu-id="2b005-117">Określa nazwę zalecanej akcji, dla której to polecenie cmdlet aktualizuje stan.</span><span class="sxs-lookup"><span data-stu-id="2b005-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="2b005-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b005-118">-ResourceGroupName</span></span>
<span data-ttu-id="2b005-119">Określa nazwę grupy zasobów serwera.</span><span class="sxs-lookup"><span data-stu-id="2b005-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="2b005-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2b005-120">-ServerName</span></span>
<span data-ttu-id="2b005-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="2b005-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2b005-122">— województwo</span><span class="sxs-lookup"><span data-stu-id="2b005-122">-State</span></span>
<span data-ttu-id="2b005-123">Określa nową wartość, dla której to polecenie cmdlet aktualizuje stan zalecanej akcji.</span><span class="sxs-lookup"><span data-stu-id="2b005-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="2b005-124">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2b005-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b005-125">Aktywny</span><span class="sxs-lookup"><span data-stu-id="2b005-125">Active</span></span>
- <span data-ttu-id="2b005-126">Oczekiwanie</span><span class="sxs-lookup"><span data-stu-id="2b005-126">Pending</span></span>
- <span data-ttu-id="2b005-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="2b005-127">PendingRevert</span></span>
- <span data-ttu-id="2b005-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="2b005-128">RevertCancelled</span></span>
- <span data-ttu-id="2b005-129">Ignorowane</span><span class="sxs-lookup"><span data-stu-id="2b005-129">Ignored</span></span>
- <span data-ttu-id="2b005-130">Rozwiązano</span><span class="sxs-lookup"><span data-stu-id="2b005-130">Resolved</span></span>

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

### <span data-ttu-id="2b005-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b005-131">-Confirm</span></span>
<span data-ttu-id="2b005-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2b005-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b005-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b005-133">-WhatIf</span></span>
<span data-ttu-id="2b005-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b005-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b005-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2b005-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b005-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b005-136">CommonParameters</span></span>
<span data-ttu-id="2b005-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b005-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b005-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b005-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b005-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b005-139">INPUTS</span></span>

### <span data-ttu-id="2b005-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2b005-140">System.String</span></span>

### <span data-ttu-id="2b005-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="2b005-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="2b005-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b005-142">OUTPUTS</span></span>

### <span data-ttu-id="2b005-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecomctionActionModel</span><span class="sxs-lookup"><span data-stu-id="2b005-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="2b005-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2b005-144">NOTES</span></span>
* <span data-ttu-id="2b005-145">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="2b005-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="2b005-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b005-146">RELATED LINKS</span></span>

[<span data-ttu-id="2b005-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="2b005-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="2b005-148">Get-AzSqlServerRecomctionAction</span><span class="sxs-lookup"><span data-stu-id="2b005-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="2b005-149">Set-AzSqlDatabaseRecomctionActionState</span><span class="sxs-lookup"><span data-stu-id="2b005-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="2b005-150">Set-AzSqlElasticPoolRecomctionActionState</span><span class="sxs-lookup"><span data-stu-id="2b005-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="2b005-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2b005-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
