---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233918"
---
# <span data-ttu-id="0daec-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="0daec-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="0daec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0daec-102">SYNOPSIS</span></span>
<span data-ttu-id="0daec-103">Umożliwia wykonanie co najmniej jednego wykonania kroku zadania</span><span class="sxs-lookup"><span data-stu-id="0daec-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="0daec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0daec-104">SYNTAX</span></span>

### <span data-ttu-id="0daec-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0daec-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0daec-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="0daec-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0daec-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="0daec-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0daec-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0daec-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0daec-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0daec-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0daec-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0daec-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0daec-111">Opis</span><span class="sxs-lookup"><span data-stu-id="0daec-111">DESCRIPTION</span></span>
<span data-ttu-id="0daec-112">Polecenie cmdlet Get-AzSqlElasticJobStepExecution umożliwia wykonanie co najmniej jednego kroku wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="0daec-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="0daec-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0daec-113">EXAMPLES</span></span>

### <span data-ttu-id="0daec-114">Przykład 1-umożliwia wykonanie co najmniej jednego wykonania kroku zadania z wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="0daec-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="0daec-115">Przykład 2 — umożliwia wykonanie co najmniej jednego wykonania kroku zadania w trakcie wykonywania zadania, filtrowanie według nazwy kroku</span><span class="sxs-lookup"><span data-stu-id="0daec-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="0daec-116">Umożliwia wykonanie co najmniej jednego wykonania kroku zadania</span><span class="sxs-lookup"><span data-stu-id="0daec-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="0daec-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0daec-117">PARAMETERS</span></span>

### <span data-ttu-id="0daec-118">— Aktywne</span><span class="sxs-lookup"><span data-stu-id="0daec-118">-Active</span></span>
<span data-ttu-id="0daec-119">Flaga filtrowania według aktywnych operacji.</span><span class="sxs-lookup"><span data-stu-id="0daec-119">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="0daec-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0daec-120">-AgentName</span></span>
<span data-ttu-id="0daec-121">Nazwa agenta.</span><span class="sxs-lookup"><span data-stu-id="0daec-121">The agent name.</span></span>

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

### <span data-ttu-id="0daec-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="0daec-122">-CreateTimeMax</span></span>
<span data-ttu-id="0daec-123">Filtruj według — Utwórz maks. czas</span><span class="sxs-lookup"><span data-stu-id="0daec-123">Filter by create time max</span></span>

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

### <span data-ttu-id="0daec-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="0daec-124">-CreateTimeMin</span></span>
<span data-ttu-id="0daec-125">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="0daec-125">Filter by create time min</span></span>

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

### <span data-ttu-id="0daec-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0daec-126">-DefaultProfile</span></span>
<span data-ttu-id="0daec-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0daec-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0daec-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="0daec-128">-EndTimeMax</span></span>
<span data-ttu-id="0daec-129">Filtruj według godziny zakończenia, maks.</span><span class="sxs-lookup"><span data-stu-id="0daec-129">Filter by end time max.</span></span>

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

### <span data-ttu-id="0daec-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="0daec-130">-EndTimeMin</span></span>
<span data-ttu-id="0daec-131">Filtruj według godziny zakończenia, min.</span><span class="sxs-lookup"><span data-stu-id="0daec-131">Filter by end time min.</span></span>

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

### <span data-ttu-id="0daec-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="0daec-132">-JobExecutionId</span></span>
<span data-ttu-id="0daec-133">Identyfikator wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="0daec-133">The job execution id.</span></span>

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

### <span data-ttu-id="0daec-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="0daec-134">-JobName</span></span>
<span data-ttu-id="0daec-135">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="0daec-135">The job name.</span></span>

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

### <span data-ttu-id="0daec-136">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="0daec-136">-ParentObject</span></span>
<span data-ttu-id="0daec-137">Obiekt Agent.</span><span class="sxs-lookup"><span data-stu-id="0daec-137">The agent object.</span></span>

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

### <span data-ttu-id="0daec-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0daec-138">-ParentResourceId</span></span>
<span data-ttu-id="0daec-139">Identyfikator zasobu wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="0daec-139">The job execution resource id.</span></span>

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

### <span data-ttu-id="0daec-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0daec-140">-ResourceGroupName</span></span>
<span data-ttu-id="0daec-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0daec-141">The resource group name.</span></span>

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

### <span data-ttu-id="0daec-142">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0daec-142">-ServerName</span></span>
<span data-ttu-id="0daec-143">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0daec-143">The server name.</span></span>

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

### <span data-ttu-id="0daec-144">-Krokname</span><span class="sxs-lookup"><span data-stu-id="0daec-144">-StepName</span></span>
<span data-ttu-id="0daec-145">Nazwa etapu zadania.</span><span class="sxs-lookup"><span data-stu-id="0daec-145">The job step name.</span></span>

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

### <span data-ttu-id="0daec-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0daec-146">CommonParameters</span></span>
<span data-ttu-id="0daec-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0daec-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0daec-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0daec-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0daec-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0daec-149">INPUTS</span></span>

### <span data-ttu-id="0daec-150">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="0daec-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0daec-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0daec-151">OUTPUTS</span></span>

### <span data-ttu-id="0daec-152">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="0daec-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0daec-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0daec-153">NOTES</span></span>

## <span data-ttu-id="0daec-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0daec-154">RELATED LINKS</span></span>
