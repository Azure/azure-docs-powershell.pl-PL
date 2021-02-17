---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198578"
---
# <span data-ttu-id="ab663-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="ab663-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="ab663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab663-102">SYNOPSIS</span></span>
<span data-ttu-id="ab663-103">Otrzymuje jedno lub więcej zadań wykonywania</span><span class="sxs-lookup"><span data-stu-id="ab663-103">Gets one or more job executions</span></span>

## <span data-ttu-id="ab663-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab663-104">SYNTAX</span></span>

### <span data-ttu-id="ab663-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="ab663-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab663-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="ab663-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab663-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ab663-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab663-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ab663-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab663-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ab663-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab663-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ab663-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab663-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab663-111">DESCRIPTION</span></span>
<span data-ttu-id="ab663-112">Polecenie Get-AzSqlElasticJobExecution pobiera jedno lub więcej wykonywania zadań</span><span class="sxs-lookup"><span data-stu-id="ab663-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="ab663-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab663-113">EXAMPLES</span></span>

### <span data-ttu-id="ab663-114">Przykład 1. Pobiera jedno lub więcej wykonywania zadań we wszystkich zadaniach</span><span class="sxs-lookup"><span data-stu-id="ab663-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="ab663-115">Przykład 2. Pobiera jedno lub więcej wykonywania zadań dla zadania</span><span class="sxs-lookup"><span data-stu-id="ab663-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="ab663-116">Otrzymuje jedno lub więcej zadań wykonywania</span><span class="sxs-lookup"><span data-stu-id="ab663-116">Gets one or more job executions</span></span>

### <span data-ttu-id="ab663-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ab663-117">Example 3</span></span>

<span data-ttu-id="ab663-118">Otrzymuje jedno lub więcej zadań wykonywania.</span><span class="sxs-lookup"><span data-stu-id="ab663-118">Gets one or more job executions.</span></span> <span data-ttu-id="ab663-119">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="ab663-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="ab663-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab663-120">PARAMETERS</span></span>

### <span data-ttu-id="ab663-121">— Aktywne</span><span class="sxs-lookup"><span data-stu-id="ab663-121">-Active</span></span>
<span data-ttu-id="ab663-122">Filtrowanie według czasu utworzenia</span><span class="sxs-lookup"><span data-stu-id="ab663-122">Filter by create time min</span></span>

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

### <span data-ttu-id="ab663-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ab663-123">-AgentName</span></span>
<span data-ttu-id="ab663-124">Nazwa agenta.</span><span class="sxs-lookup"><span data-stu-id="ab663-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab663-125">— Liczba</span><span class="sxs-lookup"><span data-stu-id="ab663-125">-Count</span></span>
<span data-ttu-id="ab663-126">Funkcja Licznik zwraca najwyższą liczbę wykonań.</span><span class="sxs-lookup"><span data-stu-id="ab663-126">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab663-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="ab663-127">-CreateTimeMax</span></span>
<span data-ttu-id="ab663-128">Filtrowanie według minimum czasu utworzenia</span><span class="sxs-lookup"><span data-stu-id="ab663-128">Filter by create time min</span></span>

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

### <span data-ttu-id="ab663-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="ab663-129">-CreateTimeMin</span></span>
<span data-ttu-id="ab663-130">Filtrowanie według minimum czasu utworzenia</span><span class="sxs-lookup"><span data-stu-id="ab663-130">Filter by create time min</span></span>

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

### <span data-ttu-id="ab663-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab663-131">-DefaultProfile</span></span>
<span data-ttu-id="ab663-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab663-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab663-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="ab663-133">-EndTimeMax</span></span>
<span data-ttu-id="ab663-134">Filtrowanie według minimum czasu utworzenia</span><span class="sxs-lookup"><span data-stu-id="ab663-134">Filter by create time min</span></span>

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

### <span data-ttu-id="ab663-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="ab663-135">-EndTimeMin</span></span>
<span data-ttu-id="ab663-136">Filtrowanie według minimum czasu utworzenia</span><span class="sxs-lookup"><span data-stu-id="ab663-136">Filter by create time min</span></span>

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

### <span data-ttu-id="ab663-137">- JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="ab663-137">-JobExecutionId</span></span>
<span data-ttu-id="ab663-138">Identyfikator wykonywania zadania.</span><span class="sxs-lookup"><span data-stu-id="ab663-138">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab663-139">— JobName</span><span class="sxs-lookup"><span data-stu-id="ab663-139">-JobName</span></span>
<span data-ttu-id="ab663-140">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="ab663-140">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab663-141">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="ab663-141">-ParentObject</span></span>
<span data-ttu-id="ab663-142">Identyfikator wykonywania zadania.</span><span class="sxs-lookup"><span data-stu-id="ab663-142">The job execution id.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, WithJobExecutionIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab663-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ab663-143">-ParentResourceId</span></span>
<span data-ttu-id="ab663-144">Identyfikator zasobu agenta.</span><span class="sxs-lookup"><span data-stu-id="ab663-144">The agent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab663-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab663-145">-ResourceGroupName</span></span>
<span data-ttu-id="ab663-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab663-146">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab663-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ab663-147">-ServerName</span></span>
<span data-ttu-id="ab663-148">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ab663-148">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab663-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab663-149">CommonParameters</span></span>
<span data-ttu-id="ab663-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab663-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab663-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab663-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab663-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab663-152">INPUTS</span></span>

### <span data-ttu-id="ab663-153">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="ab663-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="ab663-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab663-154">OUTPUTS</span></span>

### <span data-ttu-id="ab663-155">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="ab663-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="ab663-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab663-156">NOTES</span></span>

## <span data-ttu-id="ab663-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab663-157">RELATED LINKS</span></span>
