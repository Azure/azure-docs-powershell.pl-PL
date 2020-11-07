---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 78366f70db7bd586e1e35566f167c7cae2c2dbf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895689"
---
# <span data-ttu-id="c71f3-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c71f3-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="c71f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c71f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c71f3-103">Aktualizuje stan zalecanej akcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c71f3-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="c71f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c71f3-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c71f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c71f3-105">DESCRIPTION</span></span>
<span data-ttu-id="c71f3-106">Stan aktualizacji polecenia cmdlet **Set-AzSqlServerRecommendedActionState** dla zalecanej akcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c71f3-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="c71f3-107">To polecenie cmdlet dotyczy, przywraca lub odrzuca zalecaną akcję na podstawie nowego stanu.</span><span class="sxs-lookup"><span data-stu-id="c71f3-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="c71f3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c71f3-108">EXAMPLES</span></span>

### <span data-ttu-id="c71f3-109">Example1: zaktualizuj stan określonej zalecanej akcji do oczekujących</span><span class="sxs-lookup"><span data-stu-id="c71f3-109">Example1: Update the state of the specified recommended action to Pending</span></span>
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

<span data-ttu-id="c71f3-110">Stan aktualizacji zalecanej akcji serwera o nazwie "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" do "oczekujących"</span><span class="sxs-lookup"><span data-stu-id="c71f3-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="c71f3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c71f3-111">PARAMETERS</span></span>

### <span data-ttu-id="c71f3-112">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="c71f3-112">-AdvisorName</span></span>
<span data-ttu-id="c71f3-113">Określa nazwę klasyfikatora zawierającego zalecaną akcję.</span><span class="sxs-lookup"><span data-stu-id="c71f3-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="c71f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c71f3-114">-DefaultProfile</span></span>
<span data-ttu-id="c71f3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c71f3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c71f3-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="c71f3-116">-RecommendedActionName</span></span>
<span data-ttu-id="c71f3-117">Określa nazwę zalecanej akcji, dla której to polecenie cmdlet aktualizuje stan.</span><span class="sxs-lookup"><span data-stu-id="c71f3-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="c71f3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c71f3-118">-ResourceGroupName</span></span>
<span data-ttu-id="c71f3-119">Określa nazwę grupy zasobów serwera.</span><span class="sxs-lookup"><span data-stu-id="c71f3-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="c71f3-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c71f3-120">-ServerName</span></span>
<span data-ttu-id="c71f3-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="c71f3-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c71f3-122">-State</span><span class="sxs-lookup"><span data-stu-id="c71f3-122">-State</span></span>
<span data-ttu-id="c71f3-123">Określa nową wartość, na którą to polecenie cmdlet aktualizuje zalecany stan akcji.</span><span class="sxs-lookup"><span data-stu-id="c71f3-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="c71f3-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c71f3-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c71f3-125">Active</span><span class="sxs-lookup"><span data-stu-id="c71f3-125">Active</span></span>
- <span data-ttu-id="c71f3-126">Wybranego</span><span class="sxs-lookup"><span data-stu-id="c71f3-126">Pending</span></span>
- <span data-ttu-id="c71f3-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="c71f3-127">PendingRevert</span></span>
- <span data-ttu-id="c71f3-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="c71f3-128">RevertCancelled</span></span>
- <span data-ttu-id="c71f3-129">Zignorowała</span><span class="sxs-lookup"><span data-stu-id="c71f3-129">Ignored</span></span>
- <span data-ttu-id="c71f3-130">Rozpoznawania</span><span class="sxs-lookup"><span data-stu-id="c71f3-130">Resolved</span></span>

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

### <span data-ttu-id="c71f3-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c71f3-131">-Confirm</span></span>
<span data-ttu-id="c71f3-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c71f3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c71f3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c71f3-133">-WhatIf</span></span>
<span data-ttu-id="c71f3-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c71f3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c71f3-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c71f3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c71f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71f3-136">CommonParameters</span></span>
<span data-ttu-id="c71f3-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c71f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71f3-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c71f3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71f3-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c71f3-139">INPUTS</span></span>

### <span data-ttu-id="c71f3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c71f3-140">System.String</span></span>

### <span data-ttu-id="c71f3-141">Microsoft. Azure. Commands. SQL. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c71f3-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="c71f3-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c71f3-142">OUTPUTS</span></span>

### <span data-ttu-id="c71f3-143">Microsoft. Azure. Commands. SQL. RecommendedAction. model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="c71f3-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="c71f3-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c71f3-144">NOTES</span></span>
* <span data-ttu-id="c71f3-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Server, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="c71f3-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="c71f3-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c71f3-146">RELATED LINKS</span></span>

[<span data-ttu-id="c71f3-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="c71f3-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="c71f3-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="c71f3-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="c71f3-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c71f3-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="c71f3-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c71f3-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="c71f3-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c71f3-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
