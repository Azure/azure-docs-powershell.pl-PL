---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: d31af9321a474c1261b2ed75138696d9f1a45461
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542828"
---
# <span data-ttu-id="048a5-101">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="048a5-101">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="048a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="048a5-102">SYNOPSIS</span></span>
<span data-ttu-id="048a5-103">Aktualizuje stan zalecanej akcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="048a5-103">Updates the state of an Azure SQL Database recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="048a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="048a5-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="048a5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="048a5-105">DESCRIPTION</span></span>
<span data-ttu-id="048a5-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseRecommendedActionState** aktualizuje stan zalecanej akcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="048a5-106">The **Set-AzureRmSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="048a5-107">Umożliwia to stosowanie zalecanych akcji, przywracanych lub odrzucanych na podstawie nowego stanu.</span><span class="sxs-lookup"><span data-stu-id="048a5-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="048a5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="048a5-108">EXAMPLES</span></span>

### <span data-ttu-id="048a5-109">Przykład 1. Zastosuj zalecany stan akcji do oczekujących</span><span class="sxs-lookup"><span data-stu-id="048a5-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="048a5-110">To polecenie aktualizuje stan zalecanej akcji o nazwie IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 należącej do bazy danych o nazwie WIRunner.</span><span class="sxs-lookup"><span data-stu-id="048a5-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="048a5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="048a5-111">PARAMETERS</span></span>

### <span data-ttu-id="048a5-112">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="048a5-112">-AdvisorName</span></span>
<span data-ttu-id="048a5-113">Określa nazwę klasyfikatora, do którego należy zalecana akcja.</span><span class="sxs-lookup"><span data-stu-id="048a5-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="048a5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="048a5-114">-DatabaseName</span></span>
<span data-ttu-id="048a5-115">Określa nazwę bazy danych, dla której to polecenie cmdlet ustawia zalecany stan akcji.</span><span class="sxs-lookup"><span data-stu-id="048a5-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="048a5-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="048a5-116">-RecommendedActionName</span></span>
<span data-ttu-id="048a5-117">Określa nazwę zalecanej akcji, dla której stan jest aktualizowany.</span><span class="sxs-lookup"><span data-stu-id="048a5-117">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="048a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="048a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="048a5-119">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="048a5-119">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="048a5-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="048a5-120">-ServerName</span></span>
<span data-ttu-id="048a5-121">Określa nazwę serwera, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="048a5-121">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="048a5-122">-State</span><span class="sxs-lookup"><span data-stu-id="048a5-122">-State</span></span>
<span data-ttu-id="048a5-123">Określa nową wartość, na którą to polecenie cmdlet aktualizuje zalecany stan akcji.</span><span class="sxs-lookup"><span data-stu-id="048a5-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="048a5-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="048a5-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="048a5-125">Active</span><span class="sxs-lookup"><span data-stu-id="048a5-125">Active</span></span>
- <span data-ttu-id="048a5-126">Wybranego</span><span class="sxs-lookup"><span data-stu-id="048a5-126">Pending</span></span>
- <span data-ttu-id="048a5-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="048a5-127">PendingRevert</span></span>
- <span data-ttu-id="048a5-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="048a5-128">RevertCancelled</span></span>
- <span data-ttu-id="048a5-129">Zignorowała</span><span class="sxs-lookup"><span data-stu-id="048a5-129">Ignored</span></span>
- <span data-ttu-id="048a5-130">Rozpoznawania</span><span class="sxs-lookup"><span data-stu-id="048a5-130">Resolved</span></span>

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

### <span data-ttu-id="048a5-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="048a5-131">-Confirm</span></span>
<span data-ttu-id="048a5-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="048a5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="048a5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="048a5-133">-WhatIf</span></span>
<span data-ttu-id="048a5-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="048a5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="048a5-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="048a5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="048a5-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048a5-136">-DefaultProfile</span></span>
<span data-ttu-id="048a5-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="048a5-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="048a5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048a5-138">CommonParameters</span></span>
<span data-ttu-id="048a5-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048a5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048a5-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="048a5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048a5-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="048a5-141">INPUTS</span></span>

## <span data-ttu-id="048a5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="048a5-142">OUTPUTS</span></span>

### <span data-ttu-id="048a5-143">Microsoft. Azure. Commands. SQL. RecommendedAction. model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="048a5-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="048a5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="048a5-144">NOTES</span></span>
* <span data-ttu-id="048a5-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="048a5-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="048a5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="048a5-146">RELATED LINKS</span></span>

[<span data-ttu-id="048a5-147">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="048a5-147">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="048a5-148">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="048a5-148">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="048a5-149">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="048a5-149">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="048a5-150">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="048a5-150">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="048a5-151">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="048a5-151">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="048a5-152">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="048a5-152">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="048a5-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="048a5-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="048a5-154">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="048a5-154">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="048a5-155">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="048a5-155">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="048a5-156">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="048a5-156">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="048a5-157">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="048a5-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
