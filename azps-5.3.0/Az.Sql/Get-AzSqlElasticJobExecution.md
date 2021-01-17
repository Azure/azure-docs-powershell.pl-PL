---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374810"
---
# <span data-ttu-id="185d6-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="185d6-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="185d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="185d6-102">SYNOPSIS</span></span>
<span data-ttu-id="185d6-103">Pobiera co najmniej jedno wykonanie zadania</span><span class="sxs-lookup"><span data-stu-id="185d6-103">Gets one or more job executions</span></span>

## <span data-ttu-id="185d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="185d6-104">SYNTAX</span></span>

### <span data-ttu-id="185d6-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="185d6-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="185d6-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="185d6-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="185d6-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="185d6-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="185d6-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="185d6-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="185d6-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="185d6-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="185d6-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="185d6-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="185d6-111">Opis</span><span class="sxs-lookup"><span data-stu-id="185d6-111">DESCRIPTION</span></span>
<span data-ttu-id="185d6-112">Polecenie cmdlet Get-AzSqlElasticJobExecution umożliwia wykonanie co najmniej jednego wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="185d6-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="185d6-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="185d6-113">EXAMPLES</span></span>

### <span data-ttu-id="185d6-114">Przykład 1: umożliwia wykonanie jednego lub większej liczby wykonań zadań we wszystkich zadaniach</span><span class="sxs-lookup"><span data-stu-id="185d6-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="185d6-115">Przykład 2: umożliwia wykonanie co najmniej jednego zadania wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="185d6-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="185d6-116">Pobiera co najmniej jedno wykonanie zadania</span><span class="sxs-lookup"><span data-stu-id="185d6-116">Gets one or more job executions</span></span>

### <span data-ttu-id="185d6-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="185d6-117">Example 3</span></span>

<span data-ttu-id="185d6-118">Umożliwia wykonanie co najmniej jednego wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="185d6-118">Gets one or more job executions.</span></span> <span data-ttu-id="185d6-119">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="185d6-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="185d6-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="185d6-120">PARAMETERS</span></span>

### <span data-ttu-id="185d6-121">— Aktywne</span><span class="sxs-lookup"><span data-stu-id="185d6-121">-Active</span></span>
<span data-ttu-id="185d6-122">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="185d6-122">Filter by create time min</span></span>

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

### <span data-ttu-id="185d6-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="185d6-123">-AgentName</span></span>
<span data-ttu-id="185d6-124">Nazwa agenta.</span><span class="sxs-lookup"><span data-stu-id="185d6-124">The agent name.</span></span>

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

### <span data-ttu-id="185d6-125">-Count</span><span class="sxs-lookup"><span data-stu-id="185d6-125">-Count</span></span>
<span data-ttu-id="185d6-126">Funkcja count zwraca liczbę pierwszych wykonań.</span><span class="sxs-lookup"><span data-stu-id="185d6-126">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="185d6-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="185d6-127">-CreateTimeMax</span></span>
<span data-ttu-id="185d6-128">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="185d6-128">Filter by create time min</span></span>

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

### <span data-ttu-id="185d6-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="185d6-129">-CreateTimeMin</span></span>
<span data-ttu-id="185d6-130">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="185d6-130">Filter by create time min</span></span>

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

### <span data-ttu-id="185d6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185d6-131">-DefaultProfile</span></span>
<span data-ttu-id="185d6-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="185d6-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="185d6-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="185d6-133">-EndTimeMax</span></span>
<span data-ttu-id="185d6-134">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="185d6-134">Filter by create time min</span></span>

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

### <span data-ttu-id="185d6-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="185d6-135">-EndTimeMin</span></span>
<span data-ttu-id="185d6-136">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="185d6-136">Filter by create time min</span></span>

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

### <span data-ttu-id="185d6-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="185d6-137">-JobExecutionId</span></span>
<span data-ttu-id="185d6-138">Identyfikator wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="185d6-138">The job execution id.</span></span>

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

### <span data-ttu-id="185d6-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="185d6-139">-JobName</span></span>
<span data-ttu-id="185d6-140">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="185d6-140">The job name.</span></span>

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

### <span data-ttu-id="185d6-141">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="185d6-141">-ParentObject</span></span>
<span data-ttu-id="185d6-142">Identyfikator wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="185d6-142">The job execution id.</span></span>

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

### <span data-ttu-id="185d6-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="185d6-143">-ParentResourceId</span></span>
<span data-ttu-id="185d6-144">Identyfikator zasobu agenta.</span><span class="sxs-lookup"><span data-stu-id="185d6-144">The agent resource id.</span></span>

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

### <span data-ttu-id="185d6-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="185d6-145">-ResourceGroupName</span></span>
<span data-ttu-id="185d6-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="185d6-146">The resource group name.</span></span>

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

### <span data-ttu-id="185d6-147">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="185d6-147">-ServerName</span></span>
<span data-ttu-id="185d6-148">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="185d6-148">The server name.</span></span>

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

### <span data-ttu-id="185d6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185d6-149">CommonParameters</span></span>
<span data-ttu-id="185d6-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="185d6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185d6-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="185d6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185d6-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="185d6-152">INPUTS</span></span>

### <span data-ttu-id="185d6-153">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="185d6-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="185d6-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="185d6-154">OUTPUTS</span></span>

### <span data-ttu-id="185d6-155">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="185d6-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="185d6-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="185d6-156">NOTES</span></span>

## <span data-ttu-id="185d6-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="185d6-157">RELATED LINKS</span></span>
