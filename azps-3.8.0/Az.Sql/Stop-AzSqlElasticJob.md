---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ff117dfee7f660845389bd62245be4ecfd53b2f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895637"
---
# <span data-ttu-id="a9149-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="a9149-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="a9149-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9149-102">SYNOPSIS</span></span>
<span data-ttu-id="a9149-103">Zatrzymuje zadanie o identyfikatorze wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="a9149-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="a9149-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9149-104">SYNTAX</span></span>

### <span data-ttu-id="a9149-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9149-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9149-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="a9149-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9149-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9149-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9149-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9149-108">DESCRIPTION</span></span>
<span data-ttu-id="a9149-109">Polecenie cmdlet Stop-AzSqlElasticJob zatrzymuje zadanie z uruchomionym wykonaniem.</span><span class="sxs-lookup"><span data-stu-id="a9149-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="a9149-110">Zwraca bieżący stan wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="a9149-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="a9149-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9149-111">EXAMPLES</span></span>

### <span data-ttu-id="a9149-112">Przykład 1-zatrzymuje zadanie z uruchomionym wykonaniem zadania</span><span class="sxs-lookup"><span data-stu-id="a9149-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="a9149-113">Zatrzymuje uruchomione zadanie wykonania zadania i zwraca jego bieżący stan.</span><span class="sxs-lookup"><span data-stu-id="a9149-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="a9149-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9149-114">PARAMETERS</span></span>

### <span data-ttu-id="a9149-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a9149-115">-AgentName</span></span>
<span data-ttu-id="a9149-116">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="a9149-116">The agent name</span></span>

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

### <span data-ttu-id="a9149-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9149-117">-DefaultProfile</span></span>
<span data-ttu-id="a9149-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9149-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9149-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="a9149-119">-JobExecutionId</span></span>
<span data-ttu-id="a9149-120">Identyfikator wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="a9149-120">The job execution id.</span></span>

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

### <span data-ttu-id="a9149-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="a9149-121">-JobName</span></span>
<span data-ttu-id="a9149-122">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="a9149-122">The job name</span></span>

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

### <span data-ttu-id="a9149-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="a9149-123">-ParentObject</span></span>
<span data-ttu-id="a9149-124">Obiekt bazy danych kontroli agenta</span><span class="sxs-lookup"><span data-stu-id="a9149-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="a9149-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a9149-125">-ParentResourceId</span></span>
<span data-ttu-id="a9149-126">Identyfikator zasobu wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="a9149-126">The job execution resource id</span></span>

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

### <span data-ttu-id="a9149-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9149-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9149-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9149-128">The resource group name</span></span>

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

### <span data-ttu-id="a9149-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a9149-129">-ServerName</span></span>
<span data-ttu-id="a9149-130">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="a9149-130">The server name</span></span>

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

### <span data-ttu-id="a9149-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9149-131">-Confirm</span></span>
<span data-ttu-id="a9149-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9149-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9149-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9149-133">-WhatIf</span></span>
<span data-ttu-id="a9149-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9149-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9149-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9149-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9149-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9149-136">CommonParameters</span></span>
<span data-ttu-id="a9149-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9149-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9149-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9149-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9149-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9149-139">INPUTS</span></span>

### <span data-ttu-id="a9149-140">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="a9149-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="a9149-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9149-141">OUTPUTS</span></span>

### <span data-ttu-id="a9149-142">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="a9149-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="a9149-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9149-143">NOTES</span></span>

## <span data-ttu-id="a9149-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9149-144">RELATED LINKS</span></span>
