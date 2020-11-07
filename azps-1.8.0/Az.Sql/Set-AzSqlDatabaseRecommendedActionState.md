---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 49ea5796e8f2b03fe67a6c40ab42dc7f1c2481e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707757"
---
# <span data-ttu-id="769c8-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="769c8-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="769c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="769c8-102">SYNOPSIS</span></span>
<span data-ttu-id="769c8-103">Aktualizuje stan zalecanej akcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="769c8-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="769c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="769c8-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="769c8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="769c8-105">DESCRIPTION</span></span>
<span data-ttu-id="769c8-106">Polecenie cmdlet **Set-AzSqlDatabaseRecommendedActionState** aktualizuje stan zalecanej akcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="769c8-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="769c8-107">Umożliwia to stosowanie zalecanych akcji, przywracanych lub odrzucanych na podstawie nowego stanu.</span><span class="sxs-lookup"><span data-stu-id="769c8-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="769c8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="769c8-108">EXAMPLES</span></span>

### <span data-ttu-id="769c8-109">Przykład 1. Zastosuj zalecany stan akcji do oczekujących</span><span class="sxs-lookup"><span data-stu-id="769c8-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="769c8-110">To polecenie aktualizuje stan zalecanej akcji o nazwie IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 należącej do bazy danych o nazwie WIRunner.</span><span class="sxs-lookup"><span data-stu-id="769c8-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="769c8-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="769c8-111">PARAMETERS</span></span>

### <span data-ttu-id="769c8-112">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="769c8-112">-AdvisorName</span></span>
<span data-ttu-id="769c8-113">Określa nazwę klasyfikatora, do którego należy zalecana akcja.</span><span class="sxs-lookup"><span data-stu-id="769c8-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="769c8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="769c8-114">-DatabaseName</span></span>
<span data-ttu-id="769c8-115">Określa nazwę bazy danych, dla której to polecenie cmdlet ustawia zalecany stan akcji.</span><span class="sxs-lookup"><span data-stu-id="769c8-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="769c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="769c8-116">-DefaultProfile</span></span>
<span data-ttu-id="769c8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="769c8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="769c8-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="769c8-118">-RecommendedActionName</span></span>
<span data-ttu-id="769c8-119">Określa nazwę zalecanej akcji, dla której stan jest aktualizowany.</span><span class="sxs-lookup"><span data-stu-id="769c8-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="769c8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="769c8-120">-ResourceGroupName</span></span>
<span data-ttu-id="769c8-121">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="769c8-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="769c8-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="769c8-122">-ServerName</span></span>
<span data-ttu-id="769c8-123">Określa nazwę serwera, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="769c8-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="769c8-124">-State</span><span class="sxs-lookup"><span data-stu-id="769c8-124">-State</span></span>
<span data-ttu-id="769c8-125">Określa nową wartość, na którą to polecenie cmdlet aktualizuje zalecany stan akcji.</span><span class="sxs-lookup"><span data-stu-id="769c8-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="769c8-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="769c8-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="769c8-127">Active</span><span class="sxs-lookup"><span data-stu-id="769c8-127">Active</span></span>
- <span data-ttu-id="769c8-128">Wybranego</span><span class="sxs-lookup"><span data-stu-id="769c8-128">Pending</span></span>
- <span data-ttu-id="769c8-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="769c8-129">PendingRevert</span></span>
- <span data-ttu-id="769c8-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="769c8-130">RevertCancelled</span></span>
- <span data-ttu-id="769c8-131">Zignorowała</span><span class="sxs-lookup"><span data-stu-id="769c8-131">Ignored</span></span>
- <span data-ttu-id="769c8-132">Rozpoznawania</span><span class="sxs-lookup"><span data-stu-id="769c8-132">Resolved</span></span>

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

### <span data-ttu-id="769c8-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="769c8-133">-Confirm</span></span>
<span data-ttu-id="769c8-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="769c8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="769c8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="769c8-135">-WhatIf</span></span>
<span data-ttu-id="769c8-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="769c8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="769c8-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="769c8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="769c8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="769c8-138">CommonParameters</span></span>
<span data-ttu-id="769c8-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="769c8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="769c8-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="769c8-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="769c8-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="769c8-141">INPUTS</span></span>

### <span data-ttu-id="769c8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="769c8-142">System.String</span></span>

### <span data-ttu-id="769c8-143">Microsoft. Azure. Commands. SQL. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="769c8-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="769c8-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="769c8-144">OUTPUTS</span></span>

### <span data-ttu-id="769c8-145">Microsoft. Azure. Commands. SQL. RecommendedAction. model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="769c8-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="769c8-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="769c8-146">NOTES</span></span>
* <span data-ttu-id="769c8-147">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="769c8-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="769c8-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="769c8-148">RELATED LINKS</span></span>

[<span data-ttu-id="769c8-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="769c8-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="769c8-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="769c8-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="769c8-151">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="769c8-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="769c8-152">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="769c8-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="769c8-153">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="769c8-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="769c8-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="769c8-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="769c8-155">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="769c8-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="769c8-156">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="769c8-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="769c8-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="769c8-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="769c8-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="769c8-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="769c8-159">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="769c8-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)