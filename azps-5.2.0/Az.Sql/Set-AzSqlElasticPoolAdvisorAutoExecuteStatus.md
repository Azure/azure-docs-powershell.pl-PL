---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5e26be318f439556a7083dc4d2bcde154083f5e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337201"
---
# <span data-ttu-id="da84a-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="da84a-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="da84a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da84a-102">SYNOPSIS</span></span>
<span data-ttu-id="da84a-103">Aktualizuje stan automatycznego wykonania klasyfikatora Elastic Pool SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da84a-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="da84a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da84a-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da84a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da84a-105">DESCRIPTION</span></span>
<span data-ttu-id="da84a-106">Polecenie cmdlet **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** ustawia właściwość AutoExecute dla klasyfikatora Elastic Pool SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da84a-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="da84a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da84a-107">EXAMPLES</span></span>

### <span data-ttu-id="da84a-108">Przykład 1: Włączanie automatycznego wykonywania dla klasyfikatora</span><span class="sxs-lookup"><span data-stu-id="da84a-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="da84a-109">To polecenie ustawia stan automatycznego wykonania klasyfikatora o nazwie "Moja indeks" na włączony.</span><span class="sxs-lookup"><span data-stu-id="da84a-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="da84a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da84a-110">PARAMETERS</span></span>

### <span data-ttu-id="da84a-111">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="da84a-111">-AdvisorName</span></span>
<span data-ttu-id="da84a-112">Określa nazwę klasyfikatora, dla którego to polecenie cmdlet aktualizuje stan automatycznego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="da84a-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="da84a-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="da84a-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="da84a-114">Określa nową wartość, na którą to polecenie cmdlet aktualizuje stan automatycznego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="da84a-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="da84a-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="da84a-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da84a-116">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="da84a-116">Enabled</span></span>
- <span data-ttu-id="da84a-117">Łącza</span><span class="sxs-lookup"><span data-stu-id="da84a-117">Disabled</span></span>
- <span data-ttu-id="da84a-118">Domyślne</span><span class="sxs-lookup"><span data-stu-id="da84a-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da84a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da84a-119">-DefaultProfile</span></span>
<span data-ttu-id="da84a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="da84a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da84a-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="da84a-121">-ElasticPoolName</span></span>
<span data-ttu-id="da84a-122">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="da84a-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="da84a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da84a-123">-ResourceGroupName</span></span>
<span data-ttu-id="da84a-124">Określa nazwę grupy zasobów serwera, która zawiera tę pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="da84a-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="da84a-125">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="da84a-125">-ServerName</span></span>
<span data-ttu-id="da84a-126">Określa nazwę serwera, na którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="da84a-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="da84a-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da84a-127">-Confirm</span></span>
<span data-ttu-id="da84a-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da84a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da84a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da84a-129">-WhatIf</span></span>
<span data-ttu-id="da84a-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da84a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da84a-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da84a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da84a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da84a-132">CommonParameters</span></span>
<span data-ttu-id="da84a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da84a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da84a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da84a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da84a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da84a-135">INPUTS</span></span>

### <span data-ttu-id="da84a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="da84a-136">System.String</span></span>

### <span data-ttu-id="da84a-137">Microsoft. Azure. Commands. SQL. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="da84a-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="da84a-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da84a-138">OUTPUTS</span></span>

### <span data-ttu-id="da84a-139">Microsoft. Azure. Commands. SQL. Advisor. model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="da84a-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="da84a-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da84a-140">NOTES</span></span>
* <span data-ttu-id="da84a-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elastyczna Pula, MSSQL, Doradca</span><span class="sxs-lookup"><span data-stu-id="da84a-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="da84a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da84a-142">RELATED LINKS</span></span>

[<span data-ttu-id="da84a-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="da84a-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="da84a-144">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="da84a-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
