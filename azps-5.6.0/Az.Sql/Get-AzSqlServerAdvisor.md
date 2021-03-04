---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: b3efbc4fdfcc5869e44d1044648152c22b679639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982129"
---
# <span data-ttu-id="a213b-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="a213b-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="a213b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a213b-102">SYNOPSIS</span></span>
<span data-ttu-id="a213b-103">Otrzymuje co najmniej jednego doradcę w usłudze Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a213b-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="a213b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a213b-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a213b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a213b-105">DESCRIPTION</span></span>
<span data-ttu-id="a213b-106">Polecenie **cmdlet Get-AzSqlServerAdvisor** pobiera co najmniej jednego doradcę programu Azure SQL Server w programie Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a213b-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="a213b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a213b-107">EXAMPLES</span></span>

### <span data-ttu-id="a213b-108">Przykład 1. Lista wszystkich doradców serwera</span><span class="sxs-lookup"><span data-stu-id="a213b-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

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

<span data-ttu-id="a213b-109">To polecenie pobiera listę wszystkich doradców serwera o nazwie wi-biegacz-australia-wschód, który należy do grupy zasobów o nazwie WIRunnersProd.</span><span class="sxs-lookup"><span data-stu-id="a213b-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="a213b-110">Przykład 2. Uzyskiwanie pojedynczego doradcy serwera</span><span class="sxs-lookup"><span data-stu-id="a213b-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="a213b-111">To polecenie pobiera doradcę o nazwie CreateIndex dla serwera o nazwie wi-biegacz-australia-wschód.</span><span class="sxs-lookup"><span data-stu-id="a213b-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="a213b-112">Przykład 3. Lista wszystkich doradców z ich zalecanymi działaniami uwzględnionych w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="a213b-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
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

<span data-ttu-id="a213b-113">To polecenie pobiera wszystkich doradców serwera o nazwie wi-sprinter-australia-east.</span><span class="sxs-lookup"><span data-stu-id="a213b-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="a213b-114">Polecenie używa parametru *ExpandRecomctionsActions,* więc polecenie cmdlet pobiera polecane przez doradców akcje zawarte w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="a213b-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="a213b-115">Przykład 4. Uzyskiwanie pojedynczego doradcy z zalecanymi działaniami uwzględnionych w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="a213b-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="a213b-116">To polecenie pobiera doradcę o nazwie CreateIndex z serwera o nazwie wi-biegacz-australia-wschód z zalecanymi akcjami uwzględnionymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="a213b-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="a213b-117">Przykład 5. Lista wszystkich doradców serwera przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="a213b-117">Example 5: List all the advisors for the server using filtering</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName d*
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

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

<span data-ttu-id="a213b-118">To polecenie otrzymuje listę wszystkich doradców serwera o nazwie wi-biegacz-australia-wschód, który należy do grupy zasobów o nazwie WIRunnersProd, której nazwa rozpoczyna się od litery "d".</span><span class="sxs-lookup"><span data-stu-id="a213b-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="a213b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a213b-119">PARAMETERS</span></span>

### <span data-ttu-id="a213b-120">- AdvisorName</span><span class="sxs-lookup"><span data-stu-id="a213b-120">-AdvisorName</span></span>
<span data-ttu-id="a213b-121">Określa nazwę doradcy, do otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a213b-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a213b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a213b-122">-DefaultProfile</span></span>
<span data-ttu-id="a213b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a213b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a213b-124">-ExpandRecomctionActions</span><span class="sxs-lookup"><span data-stu-id="a213b-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="a213b-125">Wskazuje, że polecenie cmdlet zawiera zalecane działania doradców zawarte w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="a213b-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="a213b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a213b-126">-ResourceGroupName</span></span>
<span data-ttu-id="a213b-127">Określa nazwę grupy zasobów serwera.</span><span class="sxs-lookup"><span data-stu-id="a213b-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="a213b-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a213b-128">-ServerName</span></span>
<span data-ttu-id="a213b-129">Określa nazwę serwera doradcy, o który prosi to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a213b-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="a213b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a213b-130">CommonParameters</span></span>
<span data-ttu-id="a213b-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a213b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a213b-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a213b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a213b-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a213b-133">INPUTS</span></span>

### <span data-ttu-id="a213b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a213b-134">System.String</span></span>

### <span data-ttu-id="a213b-135">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="a213b-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a213b-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a213b-136">OUTPUTS</span></span>

### <span data-ttu-id="a213b-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="a213b-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="a213b-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a213b-138">NOTES</span></span>
* <span data-ttu-id="a213b-139">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, server, mssql, doradca</span><span class="sxs-lookup"><span data-stu-id="a213b-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="a213b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a213b-140">RELATED LINKS</span></span>

[<span data-ttu-id="a213b-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="a213b-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="a213b-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="a213b-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="a213b-143">Get-AzSqlServerRecomctionAction</span><span class="sxs-lookup"><span data-stu-id="a213b-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="a213b-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a213b-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="a213b-145">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a213b-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

