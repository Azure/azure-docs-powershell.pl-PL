---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
ms.openlocfilehash: ec44664db9a0e07d963a8db289b6e91b4e76b13a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543356"
---
# <span data-ttu-id="0b742-101">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="0b742-101">Set-AzureRmSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="0b742-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b742-102">SYNOPSIS</span></span>
<span data-ttu-id="0b742-103">Aktualizuje stan zalecanej akcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0b742-103">Updates the state of an Azure SQL Server recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b742-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b742-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b742-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b742-105">DESCRIPTION</span></span>
<span data-ttu-id="0b742-106">Stan aktualizacji polecenia cmdlet **Set-AzureRmSqlServerRecommendedActionState** dla zalecanej akcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0b742-106">The **Set-AzureRmSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="0b742-107">To polecenie cmdlet dotyczy, przywraca lub odrzuca zalecaną akcję na podstawie nowego stanu.</span><span class="sxs-lookup"><span data-stu-id="0b742-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="0b742-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b742-108">EXAMPLES</span></span>

### <span data-ttu-id="0b742-109">Example1: zaktualizuj stan określonej zalecanej akcji do oczekujących</span><span class="sxs-lookup"><span data-stu-id="0b742-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="0b742-110">Stan aktualizacji zalecanej akcji serwera o nazwie "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" do "oczekujących"</span><span class="sxs-lookup"><span data-stu-id="0b742-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="0b742-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b742-111">PARAMETERS</span></span>

### <span data-ttu-id="0b742-112">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="0b742-112">-AdvisorName</span></span>
<span data-ttu-id="0b742-113">Określa nazwę klasyfikatora zawierającego zalecaną akcję.</span><span class="sxs-lookup"><span data-stu-id="0b742-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="0b742-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b742-114">-DefaultProfile</span></span>
<span data-ttu-id="0b742-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0b742-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b742-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="0b742-116">-RecommendedActionName</span></span>
<span data-ttu-id="0b742-117">Określa nazwę zalecanej akcji, dla której to polecenie cmdlet aktualizuje stan.</span><span class="sxs-lookup"><span data-stu-id="0b742-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="0b742-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b742-118">-ResourceGroupName</span></span>
<span data-ttu-id="0b742-119">Określa nazwę grupy zasobów serwera.</span><span class="sxs-lookup"><span data-stu-id="0b742-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="0b742-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0b742-120">-ServerName</span></span>
<span data-ttu-id="0b742-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="0b742-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="0b742-122">-State</span><span class="sxs-lookup"><span data-stu-id="0b742-122">-State</span></span>
<span data-ttu-id="0b742-123">Określa nową wartość, na którą to polecenie cmdlet aktualizuje zalecany stan akcji.</span><span class="sxs-lookup"><span data-stu-id="0b742-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="0b742-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b742-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b742-125">Active</span><span class="sxs-lookup"><span data-stu-id="0b742-125">Active</span></span>
- <span data-ttu-id="0b742-126">Wybranego</span><span class="sxs-lookup"><span data-stu-id="0b742-126">Pending</span></span>
- <span data-ttu-id="0b742-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="0b742-127">PendingRevert</span></span>
- <span data-ttu-id="0b742-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="0b742-128">RevertCancelled</span></span>
- <span data-ttu-id="0b742-129">Zignorowała</span><span class="sxs-lookup"><span data-stu-id="0b742-129">Ignored</span></span>
- <span data-ttu-id="0b742-130">Rozpoznawania</span><span class="sxs-lookup"><span data-stu-id="0b742-130">Resolved</span></span>

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

### <span data-ttu-id="0b742-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b742-131">-Confirm</span></span>
<span data-ttu-id="0b742-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b742-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b742-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b742-133">-WhatIf</span></span>
<span data-ttu-id="0b742-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b742-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b742-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0b742-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b742-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b742-136">CommonParameters</span></span>
<span data-ttu-id="0b742-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b742-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b742-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b742-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b742-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b742-139">INPUTS</span></span>

### <span data-ttu-id="0b742-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0b742-140">System.String</span></span>

### <span data-ttu-id="0b742-141">Microsoft. Azure. Commands. SQL. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="0b742-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="0b742-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b742-142">OUTPUTS</span></span>

### <span data-ttu-id="0b742-143">Microsoft. Azure. Commands. SQL. RecommendedAction. model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="0b742-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="0b742-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b742-144">NOTES</span></span>
* <span data-ttu-id="0b742-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Server, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="0b742-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="0b742-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b742-146">RELATED LINKS</span></span>

[<span data-ttu-id="0b742-147">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="0b742-147">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="0b742-148">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="0b742-148">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="0b742-149">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="0b742-149">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="0b742-150">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="0b742-150">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="0b742-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0b742-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
