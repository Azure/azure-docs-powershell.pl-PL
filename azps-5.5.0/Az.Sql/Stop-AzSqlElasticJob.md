---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241923"
---
# <span data-ttu-id="d3b32-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="d3b32-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="d3b32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3b32-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b32-103">Zatrzymuje zadanie, gdy jest ono identyfikatorem wykonywania zadania</span><span class="sxs-lookup"><span data-stu-id="d3b32-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="d3b32-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3b32-104">SYNTAX</span></span>

### <span data-ttu-id="d3b32-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="d3b32-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3b32-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d3b32-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3b32-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d3b32-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3b32-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3b32-108">DESCRIPTION</span></span>
<span data-ttu-id="d3b32-109">Polecenie Stop-AzSqlElasticJob cmdlet zatrzymuje uruchomione wykonywanie zadania.</span><span class="sxs-lookup"><span data-stu-id="d3b32-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="d3b32-110">Zwraca bieżący stan wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="d3b32-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="d3b32-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3b32-111">EXAMPLES</span></span>

### <span data-ttu-id="d3b32-112">Przykład 1. Zatrzymanie zadania z uruchomionym wykonaniem zadania</span><span class="sxs-lookup"><span data-stu-id="d3b32-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="d3b32-113">Zatrzymuje uruchamianie zadania i zwraca jego bieżący stan</span><span class="sxs-lookup"><span data-stu-id="d3b32-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="d3b32-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d3b32-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="d3b32-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3b32-115">PARAMETERS</span></span>

### <span data-ttu-id="d3b32-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d3b32-116">-AgentName</span></span>
<span data-ttu-id="d3b32-117">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="d3b32-117">The agent name</span></span>

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

### <span data-ttu-id="d3b32-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b32-118">-DefaultProfile</span></span>
<span data-ttu-id="d3b32-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3b32-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3b32-120">- JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="d3b32-120">-JobExecutionId</span></span>
<span data-ttu-id="d3b32-121">Identyfikator wykonywania zadania.</span><span class="sxs-lookup"><span data-stu-id="d3b32-121">The job execution id.</span></span>

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

### <span data-ttu-id="d3b32-122">— JobName</span><span class="sxs-lookup"><span data-stu-id="d3b32-122">-JobName</span></span>
<span data-ttu-id="d3b32-123">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="d3b32-123">The job name</span></span>

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

### <span data-ttu-id="d3b32-124">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="d3b32-124">-ParentObject</span></span>
<span data-ttu-id="d3b32-125">Obiekt bazy danych kontrolki agenta</span><span class="sxs-lookup"><span data-stu-id="d3b32-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="d3b32-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d3b32-126">-ParentResourceId</span></span>
<span data-ttu-id="d3b32-127">Identyfikator zasobu wykonywania zadań</span><span class="sxs-lookup"><span data-stu-id="d3b32-127">The job execution resource id</span></span>

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

### <span data-ttu-id="d3b32-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b32-128">-ResourceGroupName</span></span>
<span data-ttu-id="d3b32-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d3b32-129">The resource group name</span></span>

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

### <span data-ttu-id="d3b32-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3b32-130">-ServerName</span></span>
<span data-ttu-id="d3b32-131">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="d3b32-131">The server name</span></span>

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

### <span data-ttu-id="d3b32-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3b32-132">-Confirm</span></span>
<span data-ttu-id="d3b32-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d3b32-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3b32-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b32-134">-WhatIf</span></span>
<span data-ttu-id="d3b32-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3b32-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3b32-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d3b32-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3b32-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b32-137">CommonParameters</span></span>
<span data-ttu-id="d3b32-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3b32-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b32-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3b32-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b32-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3b32-140">INPUTS</span></span>

### <span data-ttu-id="d3b32-141">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="d3b32-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="d3b32-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3b32-142">OUTPUTS</span></span>

### <span data-ttu-id="d3b32-143">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="d3b32-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="d3b32-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3b32-144">NOTES</span></span>

## <span data-ttu-id="d3b32-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3b32-145">RELATED LINKS</span></span>
