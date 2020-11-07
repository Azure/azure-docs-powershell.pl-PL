---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 0b7fc702ad331a2ad51e1adfaf4aefd6ae440259
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887585"
---
# <span data-ttu-id="e38b9-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="e38b9-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="e38b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e38b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e38b9-103">Zatrzymuje zadanie o identyfikatorze wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="e38b9-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="e38b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e38b9-104">SYNTAX</span></span>

### <span data-ttu-id="e38b9-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e38b9-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e38b9-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="e38b9-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e38b9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e38b9-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e38b9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e38b9-108">DESCRIPTION</span></span>
<span data-ttu-id="e38b9-109">Polecenie cmdlet Stop-AzSqlElasticJob zatrzymuje zadanie z uruchomionym wykonaniem.</span><span class="sxs-lookup"><span data-stu-id="e38b9-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="e38b9-110">Zwraca bieżący stan wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="e38b9-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="e38b9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e38b9-111">EXAMPLES</span></span>

### <span data-ttu-id="e38b9-112">Przykład 1-zatrzymuje zadanie z uruchomionym wykonaniem zadania</span><span class="sxs-lookup"><span data-stu-id="e38b9-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="e38b9-113">Zatrzymuje uruchomione zadanie wykonania zadania i zwraca jego bieżący stan.</span><span class="sxs-lookup"><span data-stu-id="e38b9-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="e38b9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e38b9-114">PARAMETERS</span></span>

### <span data-ttu-id="e38b9-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e38b9-115">-AgentName</span></span>
<span data-ttu-id="e38b9-116">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="e38b9-116">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38b9-117">-DefaultProfile</span></span>
<span data-ttu-id="e38b9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e38b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e38b9-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="e38b9-119">-JobExecutionId</span></span>
<span data-ttu-id="e38b9-120">Identyfikator wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="e38b9-120">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b9-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="e38b9-121">-JobName</span></span>
<span data-ttu-id="e38b9-122">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="e38b9-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b9-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="e38b9-123">-ParentObject</span></span>
<span data-ttu-id="e38b9-124">Obiekt bazy danych kontroli agenta</span><span class="sxs-lookup"><span data-stu-id="e38b9-124">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e38b9-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e38b9-125">-ParentResourceId</span></span>
<span data-ttu-id="e38b9-126">Identyfikator zasobu wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="e38b9-126">The job execution resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e38b9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38b9-127">-ResourceGroupName</span></span>
<span data-ttu-id="e38b9-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e38b9-128">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b9-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e38b9-129">-ServerName</span></span>
<span data-ttu-id="e38b9-130">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="e38b9-130">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b9-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e38b9-131">-Confirm</span></span>
<span data-ttu-id="e38b9-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e38b9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e38b9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e38b9-133">-WhatIf</span></span>
<span data-ttu-id="e38b9-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e38b9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e38b9-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e38b9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e38b9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38b9-136">CommonParameters</span></span>
<span data-ttu-id="e38b9-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38b9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38b9-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e38b9-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38b9-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e38b9-139">INPUTS</span></span>

### <span data-ttu-id="e38b9-140">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="e38b9-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="e38b9-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e38b9-141">OUTPUTS</span></span>

### <span data-ttu-id="e38b9-142">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="e38b9-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="e38b9-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e38b9-143">NOTES</span></span>

## <span data-ttu-id="e38b9-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e38b9-144">RELATED LINKS</span></span>

## <span data-ttu-id="e38b9-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e38b9-145">RELATED LINKS</span></span>
