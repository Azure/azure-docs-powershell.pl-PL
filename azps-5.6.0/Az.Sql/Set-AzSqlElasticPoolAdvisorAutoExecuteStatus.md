---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa181dcb171a1842c2b6158078e60b717b33d579
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952986"
---
# <span data-ttu-id="8f4d9-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8f4d9-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="8f4d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4d9-103">Aktualizacje automatycznie wykonują stan doradcy puli elastycznej sql azure.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="8f4d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f4d9-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f4d9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f4d9-105">DESCRIPTION</span></span>
<span data-ttu-id="8f4d9-106">Polecenie **cmdlet Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** ustawia właściwość auto execute dla doradcy puli elastycznej języka AZURE SQL.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="8f4d9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f4d9-107">EXAMPLES</span></span>

### <span data-ttu-id="8f4d9-108">Przykład 1. Włączanie automatycznego wykonywania dla doradcy</span><span class="sxs-lookup"><span data-stu-id="8f4d9-108">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="8f4d9-109">To polecenie ustawia dla włączonego stanu automatycznego wykonywania doradcy o nazwie CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="8f4d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f4d9-110">PARAMETERS</span></span>

### <span data-ttu-id="8f4d9-111">- AdvisorName</span><span class="sxs-lookup"><span data-stu-id="8f4d9-111">-AdvisorName</span></span>
<span data-ttu-id="8f4d9-112">Określa nazwę doradcy, dla którego to polecenie cmdlet aktualizuje stan autowy wykonania.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="8f4d9-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8f4d9-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="8f4d9-114">Określa nową wartość, dla której to polecenie cmdlet aktualizuje stan autowy wykonania.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="8f4d9-115">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8f4d9-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8f4d9-116">Włączone</span><span class="sxs-lookup"><span data-stu-id="8f4d9-116">Enabled</span></span>
- <span data-ttu-id="8f4d9-117">Wyłączone</span><span class="sxs-lookup"><span data-stu-id="8f4d9-117">Disabled</span></span>
- <span data-ttu-id="8f4d9-118">Domyślne</span><span class="sxs-lookup"><span data-stu-id="8f4d9-118">Default</span></span>

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

### <span data-ttu-id="8f4d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4d9-119">-DefaultProfile</span></span>
<span data-ttu-id="8f4d9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8f4d9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f4d9-121">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="8f4d9-121">-ElasticPoolName</span></span>
<span data-ttu-id="8f4d9-122">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="8f4d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f4d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f4d9-124">Określa nazwę grupy zasobów serwera, która zawiera tę elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="8f4d9-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8f4d9-125">-ServerName</span></span>
<span data-ttu-id="8f4d9-126">Określa nazwę serwera, w którym znajduje się elastyczna pula.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="8f4d9-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f4d9-127">-Confirm</span></span>
<span data-ttu-id="8f4d9-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f4d9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f4d9-129">-WhatIf</span></span>
<span data-ttu-id="8f4d9-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f4d9-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f4d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4d9-132">CommonParameters</span></span>
<span data-ttu-id="8f4d9-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4d9-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f4d9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4d9-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f4d9-135">INPUTS</span></span>

### <span data-ttu-id="8f4d9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8f4d9-136">System.String</span></span>

### <span data-ttu-id="8f4d9-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8f4d9-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="8f4d9-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f4d9-138">OUTPUTS</span></span>

### <span data-ttu-id="8f4d9-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="8f4d9-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="8f4d9-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f4d9-140">NOTES</span></span>
* <span data-ttu-id="8f4d9-141">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, elastyczna pula, mssql, doradca</span><span class="sxs-lookup"><span data-stu-id="8f4d9-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="8f4d9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f4d9-142">RELATED LINKS</span></span>

[<span data-ttu-id="8f4d9-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="8f4d9-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="8f4d9-144">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="8f4d9-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
