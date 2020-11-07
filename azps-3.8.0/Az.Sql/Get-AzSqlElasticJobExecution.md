---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 2c4d0865ba1fb904e367857702d1344f5fb210cc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896593"
---
# <span data-ttu-id="b53f4-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="b53f4-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="b53f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b53f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b53f4-103">Pobiera co najmniej jedno wykonanie zadania</span><span class="sxs-lookup"><span data-stu-id="b53f4-103">Gets one or more job executions</span></span>

## <span data-ttu-id="b53f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b53f4-104">SYNTAX</span></span>

### <span data-ttu-id="b53f4-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b53f4-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b53f4-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="b53f4-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b53f4-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="b53f4-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b53f4-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b53f4-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b53f4-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b53f4-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b53f4-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b53f4-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b53f4-111">Opis</span><span class="sxs-lookup"><span data-stu-id="b53f4-111">DESCRIPTION</span></span>
<span data-ttu-id="b53f4-112">Polecenie cmdlet Get-AzSqlElasticJobExecution umożliwia wykonanie co najmniej jednego wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="b53f4-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="b53f4-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b53f4-113">EXAMPLES</span></span>

### <span data-ttu-id="b53f4-114">Przykład 1-umożliwia wykonanie jednego lub kilku zadań wykonywanych między wszystkimi zadaniami</span><span class="sxs-lookup"><span data-stu-id="b53f4-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="b53f4-115">Przykład 2 — umożliwia wykonanie co najmniej jednego zadania wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="b53f4-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="b53f4-116">Pobiera co najmniej jedno wykonanie zadania</span><span class="sxs-lookup"><span data-stu-id="b53f4-116">Gets one or more job executions</span></span>

## <span data-ttu-id="b53f4-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b53f4-117">PARAMETERS</span></span>

### <span data-ttu-id="b53f4-118">— Aktywne</span><span class="sxs-lookup"><span data-stu-id="b53f4-118">-Active</span></span>
<span data-ttu-id="b53f4-119">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="b53f4-119">Filter by create time min</span></span>

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

### <span data-ttu-id="b53f4-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b53f4-120">-AgentName</span></span>
<span data-ttu-id="b53f4-121">Nazwa agenta.</span><span class="sxs-lookup"><span data-stu-id="b53f4-121">The agent name.</span></span>

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

### <span data-ttu-id="b53f4-122">-Count</span><span class="sxs-lookup"><span data-stu-id="b53f4-122">-Count</span></span>
<span data-ttu-id="b53f4-123">Funkcja count zwraca liczbę pierwszych wykonań.</span><span class="sxs-lookup"><span data-stu-id="b53f4-123">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="b53f4-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="b53f4-124">-CreateTimeMax</span></span>
<span data-ttu-id="b53f4-125">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="b53f4-125">Filter by create time min</span></span>

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

### <span data-ttu-id="b53f4-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="b53f4-126">-CreateTimeMin</span></span>
<span data-ttu-id="b53f4-127">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="b53f4-127">Filter by create time min</span></span>

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

### <span data-ttu-id="b53f4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b53f4-128">-DefaultProfile</span></span>
<span data-ttu-id="b53f4-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b53f4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b53f4-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="b53f4-130">-EndTimeMax</span></span>
<span data-ttu-id="b53f4-131">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="b53f4-131">Filter by create time min</span></span>

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

### <span data-ttu-id="b53f4-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="b53f4-132">-EndTimeMin</span></span>
<span data-ttu-id="b53f4-133">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="b53f4-133">Filter by create time min</span></span>

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

### <span data-ttu-id="b53f4-134">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="b53f4-134">-JobExecutionId</span></span>
<span data-ttu-id="b53f4-135">Identyfikator wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="b53f4-135">The job execution id.</span></span>

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

### <span data-ttu-id="b53f4-136">-JobName</span><span class="sxs-lookup"><span data-stu-id="b53f4-136">-JobName</span></span>
<span data-ttu-id="b53f4-137">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="b53f4-137">The job name.</span></span>

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

### <span data-ttu-id="b53f4-138">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="b53f4-138">-ParentObject</span></span>
<span data-ttu-id="b53f4-139">Identyfikator wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="b53f4-139">The job execution id.</span></span>

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

### <span data-ttu-id="b53f4-140">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b53f4-140">-ParentResourceId</span></span>
<span data-ttu-id="b53f4-141">Identyfikator zasobu agenta.</span><span class="sxs-lookup"><span data-stu-id="b53f4-141">The agent resource id.</span></span>

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

### <span data-ttu-id="b53f4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b53f4-142">-ResourceGroupName</span></span>
<span data-ttu-id="b53f4-143">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b53f4-143">The resource group name.</span></span>

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

### <span data-ttu-id="b53f4-144">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b53f4-144">-ServerName</span></span>
<span data-ttu-id="b53f4-145">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="b53f4-145">The server name.</span></span>

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

### <span data-ttu-id="b53f4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53f4-146">CommonParameters</span></span>
<span data-ttu-id="b53f4-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b53f4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53f4-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b53f4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53f4-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b53f4-149">INPUTS</span></span>

### <span data-ttu-id="b53f4-150">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="b53f4-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b53f4-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b53f4-151">OUTPUTS</span></span>

### <span data-ttu-id="b53f4-152">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="b53f4-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="b53f4-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b53f4-153">NOTES</span></span>

## <span data-ttu-id="b53f4-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b53f4-154">RELATED LINKS</span></span>
