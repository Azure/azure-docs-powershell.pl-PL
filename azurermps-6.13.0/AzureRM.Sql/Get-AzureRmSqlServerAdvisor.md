---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvisor.md
ms.openlocfilehash: a77119e653f3d4e6155fbe98e85a583eca50c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718262"
---
# <span data-ttu-id="435e1-101">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="435e1-101">Get-AzureRmSqlServerAdvisor</span></span>

## <span data-ttu-id="435e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="435e1-102">SYNOPSIS</span></span>
<span data-ttu-id="435e1-103">Pobiera jeden lub więcej doradców dla programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="435e1-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="435e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="435e1-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="435e1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="435e1-105">DESCRIPTION</span></span>
<span data-ttu-id="435e1-106">Polecenie cmdlet **Get-AzureRmSqlServerAdvisor umożliwia pobranie** jednej lub wielu doradców programu Azure SQL Server dla programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="435e1-106">The **Get-AzureRmSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="435e1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="435e1-107">EXAMPLES</span></span>

### <span data-ttu-id="435e1-108">Przykład 1: wyświetlanie wszystkich doradców dla serwera</span><span class="sxs-lookup"><span data-stu-id="435e1-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
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

<span data-ttu-id="435e1-109">To polecenie wyświetla listę wszystkich doradców dla serwera o nazwie Wi-Runner-Australia-wschód należących do grupy zasobów o nazwie WIRunnersProd.</span><span class="sxs-lookup"><span data-stu-id="435e1-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="435e1-110">Przykład 2: uzyskiwanie jednego klasyfikatora dla serwera</span><span class="sxs-lookup"><span data-stu-id="435e1-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="435e1-111">To polecenie uzyskuje klasyfikator o nazwie Moja indeks dla serwera o nazwie Wi-Runner-Australia-wschód.</span><span class="sxs-lookup"><span data-stu-id="435e1-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="435e1-112">Przykład 3: wyświetlanie wszystkich doradców z zalecanymi działaniami zawartymi w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="435e1-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

<span data-ttu-id="435e1-113">To polecenie pobiera wszystkich doradców dla serwera o nazwie Wi-Runner-Australia-wschód.</span><span class="sxs-lookup"><span data-stu-id="435e1-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="435e1-114">Ponieważ w poleceniu jest używany parametr *ExpandRecommendedActions* , polecenie cmdlet pobiera zalecane działania doradców zawarte w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="435e1-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="435e1-115">Przykład 4: uzyskiwanie jednego klasyfikatora z zalecanymi akcjami zawartymi w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="435e1-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="435e1-116">To polecenie pobiera klasyfikator o nazwie Moja indeks z serwera o nazwie Wi-Runner-Australia-wschód z zalecanymi działaniami zawartymi w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="435e1-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

## <span data-ttu-id="435e1-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="435e1-117">PARAMETERS</span></span>

### <span data-ttu-id="435e1-118">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="435e1-118">-AdvisorName</span></span>
<span data-ttu-id="435e1-119">Określa nazwę klasyfikatora, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="435e1-119">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="435e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435e1-120">-DefaultProfile</span></span>
<span data-ttu-id="435e1-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="435e1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="435e1-122">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="435e1-122">-ExpandRecommendedActions</span></span>
<span data-ttu-id="435e1-123">Wskazuje, że polecenie cmdlet zawiera zalecane akcje doradców uwzględnionych w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="435e1-123">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="435e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="435e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="435e1-125">Określa nazwę grupy zasobów serwera.</span><span class="sxs-lookup"><span data-stu-id="435e1-125">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="435e1-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="435e1-126">-ServerName</span></span>
<span data-ttu-id="435e1-127">Określa nazwę serwera klasyfikatora, którego dotyczy żądanie polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="435e1-127">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="435e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435e1-128">CommonParameters</span></span>
<span data-ttu-id="435e1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="435e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435e1-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="435e1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435e1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="435e1-131">INPUTS</span></span>

### <span data-ttu-id="435e1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="435e1-132">System.String</span></span>

### <span data-ttu-id="435e1-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="435e1-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="435e1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="435e1-134">OUTPUTS</span></span>

### <span data-ttu-id="435e1-135">Microsoft. Azure. Commands. SQL. Advisor. model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="435e1-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="435e1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="435e1-136">NOTES</span></span>
* <span data-ttu-id="435e1-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Server, MSSQL, Doradca</span><span class="sxs-lookup"><span data-stu-id="435e1-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="435e1-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="435e1-138">RELATED LINKS</span></span>

[<span data-ttu-id="435e1-139">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="435e1-139">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="435e1-140">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="435e1-140">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="435e1-141">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="435e1-141">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="435e1-142">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="435e1-142">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="435e1-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="435e1-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

