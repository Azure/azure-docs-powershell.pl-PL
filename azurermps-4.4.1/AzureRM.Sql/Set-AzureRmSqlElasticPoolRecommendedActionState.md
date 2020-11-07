---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 1bc5d89a381027bd72697d873308eb85807a6e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718072"
---
# <span data-ttu-id="62bf2-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="62bf2-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="62bf2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="62bf2-103">Aktualizuje stan zalecanej akcji puli elastycznej w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="62bf2-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62bf2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62bf2-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62bf2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62bf2-105">DESCRIPTION</span></span>
<span data-ttu-id="62bf2-106">Stan aktualizacji polecenia cmdlet **Set-AzureRmSqlElasticPoolRecommendedActionState** w przypadku zalecanej akcji puli elastycznej w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="62bf2-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="62bf2-107">To polecenie cmdlet powoduje zastosowanie zalecanej akcji, która została przywrócona lub odrzucona na podstawie nowego stanu.</span><span class="sxs-lookup"><span data-stu-id="62bf2-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="62bf2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62bf2-108">EXAMPLES</span></span>

### <span data-ttu-id="62bf2-109">Przykład 1: aktualizowanie stanu zalecanej akcji na oczekujące</span><span class="sxs-lookup"><span data-stu-id="62bf2-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="62bf2-110">To polecenie powoduje zaktualizowanie stanu zalecanej akcji puli elastycznej o nazwie IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 na oczekujące.</span><span class="sxs-lookup"><span data-stu-id="62bf2-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="62bf2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62bf2-111">PARAMETERS</span></span>

### <span data-ttu-id="62bf2-112">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="62bf2-112">-AdvisorName</span></span>
<span data-ttu-id="62bf2-113">Określa nazwę klasyfikatora, do którego należy zalecana akcja.</span><span class="sxs-lookup"><span data-stu-id="62bf2-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="62bf2-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="62bf2-114">-ElasticPoolName</span></span>
<span data-ttu-id="62bf2-115">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="62bf2-115">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="62bf2-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="62bf2-116">-RecommendedActionName</span></span>
<span data-ttu-id="62bf2-117">Określa nazwę zalecanej akcji, dla której to polecenie cmdlet aktualizuje stan.</span><span class="sxs-lookup"><span data-stu-id="62bf2-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="62bf2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62bf2-118">-ResourceGroupName</span></span>
<span data-ttu-id="62bf2-119">Określa nazwę grupy zasobów serwera, która zawiera tę pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="62bf2-119">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="62bf2-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="62bf2-120">-ServerName</span></span>
<span data-ttu-id="62bf2-121">Określa nazwę serwera, na którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="62bf2-121">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="62bf2-122">-State</span><span class="sxs-lookup"><span data-stu-id="62bf2-122">-State</span></span>
<span data-ttu-id="62bf2-123">Określa wartość, na którą to polecenie cmdlet aktualizuje zalecany stan akcji.</span><span class="sxs-lookup"><span data-stu-id="62bf2-123">Specifies the value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="62bf2-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="62bf2-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="62bf2-125">Active</span><span class="sxs-lookup"><span data-stu-id="62bf2-125">Active</span></span>
- <span data-ttu-id="62bf2-126">Wybranego</span><span class="sxs-lookup"><span data-stu-id="62bf2-126">Pending</span></span>
- <span data-ttu-id="62bf2-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="62bf2-127">PendingRevert</span></span>
- <span data-ttu-id="62bf2-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="62bf2-128">RevertCancelled</span></span>
- <span data-ttu-id="62bf2-129">Zignorowała</span><span class="sxs-lookup"><span data-stu-id="62bf2-129">Ignored</span></span>
- <span data-ttu-id="62bf2-130">Rozpoznawania</span><span class="sxs-lookup"><span data-stu-id="62bf2-130">Resolved</span></span>

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

### <span data-ttu-id="62bf2-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62bf2-131">-Confirm</span></span>
<span data-ttu-id="62bf2-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62bf2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62bf2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62bf2-133">-WhatIf</span></span>
<span data-ttu-id="62bf2-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62bf2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62bf2-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62bf2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62bf2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bf2-136">-DefaultProfile</span></span>
<span data-ttu-id="62bf2-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62bf2-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62bf2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bf2-138">CommonParameters</span></span>
<span data-ttu-id="62bf2-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bf2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bf2-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62bf2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bf2-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62bf2-141">INPUTS</span></span>

## <span data-ttu-id="62bf2-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62bf2-142">OUTPUTS</span></span>

## <span data-ttu-id="62bf2-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62bf2-143">NOTES</span></span>
* <span data-ttu-id="62bf2-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Doradca, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="62bf2-144">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="62bf2-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62bf2-145">RELATED LINKS</span></span>

[<span data-ttu-id="62bf2-146">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="62bf2-146">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="62bf2-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="62bf2-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="62bf2-148">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="62bf2-148">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="62bf2-149">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="62bf2-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
