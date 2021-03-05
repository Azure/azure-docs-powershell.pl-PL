---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 9918c314d239bf822fa789bcab6a9de923b8c2e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999633"
---
# <span data-ttu-id="3797e-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="3797e-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="3797e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3797e-102">SYNOPSIS</span></span>
<span data-ttu-id="3797e-103">Otrzymuje co najmniej jedno wykonanie kroku zadania</span><span class="sxs-lookup"><span data-stu-id="3797e-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="3797e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3797e-104">SYNTAX</span></span>

### <span data-ttu-id="3797e-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="3797e-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3797e-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="3797e-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3797e-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3797e-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3797e-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="3797e-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3797e-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3797e-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3797e-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3797e-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3797e-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="3797e-111">DESCRIPTION</span></span>
<span data-ttu-id="3797e-112">Polecenie Get-AzSqlElasticJobStepExecution cmdlet pobiera jedno lub więcej wykonywania kroków zadania z wykonywania zadania</span><span class="sxs-lookup"><span data-stu-id="3797e-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="3797e-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3797e-113">EXAMPLES</span></span>

### <span data-ttu-id="3797e-114">Przykład 1. Pobiera jedno lub więcej wykonywania kroków zadania z wykonywania zadań</span><span class="sxs-lookup"><span data-stu-id="3797e-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="3797e-115">Przykład 2. Pobiera jedno lub więcej wykonywania kroków zadania z wykonywania zadania, filtrowanie według nazwy etapu</span><span class="sxs-lookup"><span data-stu-id="3797e-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="3797e-116">Otrzymuje co najmniej jedno wykonanie kroku zadania</span><span class="sxs-lookup"><span data-stu-id="3797e-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="3797e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3797e-117">PARAMETERS</span></span>

### <span data-ttu-id="3797e-118">— Aktywne</span><span class="sxs-lookup"><span data-stu-id="3797e-118">-Active</span></span>
<span data-ttu-id="3797e-119">Oflaguj, aby filtrować według aktywnych wykonywania.</span><span class="sxs-lookup"><span data-stu-id="3797e-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3797e-120">-AgentName</span></span>
<span data-ttu-id="3797e-121">Nazwa agenta.</span><span class="sxs-lookup"><span data-stu-id="3797e-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="3797e-122">-CreateTimeMax</span></span>
<span data-ttu-id="3797e-123">Filtrowanie według maks. czasu tworzenia</span><span class="sxs-lookup"><span data-stu-id="3797e-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="3797e-124">-CreateTimeMin</span></span>
<span data-ttu-id="3797e-125">Filtrowanie według minimum czasu utworzenia</span><span class="sxs-lookup"><span data-stu-id="3797e-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3797e-126">-DefaultProfile</span></span>
<span data-ttu-id="3797e-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3797e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3797e-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="3797e-128">-EndTimeMax</span></span>
<span data-ttu-id="3797e-129">Filtrowanie według maksymalnej godziny zakończenia.</span><span class="sxs-lookup"><span data-stu-id="3797e-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="3797e-130">-EndTimeMin</span></span>
<span data-ttu-id="3797e-131">Filtrowanie według godzin zakończenia min.</span><span class="sxs-lookup"><span data-stu-id="3797e-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-132">- JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="3797e-132">-JobExecutionId</span></span>
<span data-ttu-id="3797e-133">Identyfikator wykonywania zadania.</span><span class="sxs-lookup"><span data-stu-id="3797e-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-134">— JobName</span><span class="sxs-lookup"><span data-stu-id="3797e-134">-JobName</span></span>
<span data-ttu-id="3797e-135">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="3797e-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-136">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="3797e-136">-ParentObject</span></span>
<span data-ttu-id="3797e-137">Obiekt agenta.</span><span class="sxs-lookup"><span data-stu-id="3797e-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3797e-138">-ParentResourceId</span></span>
<span data-ttu-id="3797e-139">Identyfikator zasobu wykonywania zadań.</span><span class="sxs-lookup"><span data-stu-id="3797e-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3797e-140">-ResourceGroupName</span></span>
<span data-ttu-id="3797e-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3797e-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3797e-142">-ServerName</span></span>
<span data-ttu-id="3797e-143">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="3797e-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="3797e-144">-StepName</span></span>
<span data-ttu-id="3797e-145">Nazwa etapu zadania.</span><span class="sxs-lookup"><span data-stu-id="3797e-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3797e-146">CommonParameters</span></span>
<span data-ttu-id="3797e-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3797e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3797e-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3797e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3797e-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3797e-149">INPUTS</span></span>

### <span data-ttu-id="3797e-150">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="3797e-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="3797e-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3797e-151">OUTPUTS</span></span>

### <span data-ttu-id="3797e-152">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="3797e-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="3797e-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3797e-153">NOTES</span></span>

## <span data-ttu-id="3797e-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3797e-154">RELATED LINKS</span></span>
