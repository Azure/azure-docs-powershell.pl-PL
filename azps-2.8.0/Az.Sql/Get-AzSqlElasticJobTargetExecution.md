---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 95cd4cdfb9cc21207e336a514e91d56193119e8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886962"
---
# <span data-ttu-id="31e68-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="31e68-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="31e68-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31e68-102">SYNOPSIS</span></span>
<span data-ttu-id="31e68-103">Pobiera co najmniej jedno wykonanie zadania w celu</span><span class="sxs-lookup"><span data-stu-id="31e68-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="31e68-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31e68-104">SYNTAX</span></span>

### <span data-ttu-id="31e68-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="31e68-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31e68-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="31e68-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31e68-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="31e68-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31e68-108">Opis</span><span class="sxs-lookup"><span data-stu-id="31e68-108">DESCRIPTION</span></span>
<span data-ttu-id="31e68-109">Polecenie cmdlet Get-AzSqlElasticJobTargetExecution umożliwia pobieranie co najmniej jednego wykonania zadania w celu wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="31e68-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="31e68-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31e68-110">EXAMPLES</span></span>

### <span data-ttu-id="31e68-111">Przykład 1-umożliwia wykonanie co najmniej jednego wykonania zadania w celu wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="31e68-111">Example 1 - Gets one or more job target executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="31e68-112">Przykład 2 — pobiera co najmniej jedno wykonanie zadania w celu wykonania zadania — filtrowanie według nazwy kroku</span><span class="sxs-lookup"><span data-stu-id="31e68-112">Example 2 - Gets one or more job target executions from a job executions - filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="31e68-113">Pobiera co najmniej jedno wykonanie zadania w celu</span><span class="sxs-lookup"><span data-stu-id="31e68-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="31e68-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31e68-114">PARAMETERS</span></span>

### <span data-ttu-id="31e68-115">— Aktywne</span><span class="sxs-lookup"><span data-stu-id="31e68-115">-Active</span></span>
<span data-ttu-id="31e68-116">Flaga filtrowania według aktywnych operacji.</span><span class="sxs-lookup"><span data-stu-id="31e68-116">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="31e68-117">-AgentName</span></span>
<span data-ttu-id="31e68-118">Nazwa agenta.</span><span class="sxs-lookup"><span data-stu-id="31e68-118">The agent name.</span></span>

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

### <span data-ttu-id="31e68-119">-Count</span><span class="sxs-lookup"><span data-stu-id="31e68-119">-Count</span></span>
<span data-ttu-id="31e68-120">Funkcja count zwraca liczbę pierwszych wykonań.</span><span class="sxs-lookup"><span data-stu-id="31e68-120">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="31e68-121">-CreateTimeMax</span></span>
<span data-ttu-id="31e68-122">Filtruj według — Utwórz maks. czas</span><span class="sxs-lookup"><span data-stu-id="31e68-122">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="31e68-123">-CreateTimeMin</span></span>
<span data-ttu-id="31e68-124">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="31e68-124">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e68-125">-DefaultProfile</span></span>
<span data-ttu-id="31e68-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31e68-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31e68-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="31e68-127">-EndTimeMax</span></span>
<span data-ttu-id="31e68-128">Filtruj według godziny zakończenia, maks.</span><span class="sxs-lookup"><span data-stu-id="31e68-128">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="31e68-129">-EndTimeMin</span></span>
<span data-ttu-id="31e68-130">Filtruj według godziny zakończenia, min.</span><span class="sxs-lookup"><span data-stu-id="31e68-130">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="31e68-131">-JobExecutionId</span></span>
<span data-ttu-id="31e68-132">Identyfikator wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="31e68-132">The job execution id.</span></span>

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

### <span data-ttu-id="31e68-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="31e68-133">-JobName</span></span>
<span data-ttu-id="31e68-134">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="31e68-134">The job name.</span></span>

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

### <span data-ttu-id="31e68-135">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="31e68-135">-ParentObject</span></span>
<span data-ttu-id="31e68-136">Obiekt wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="31e68-136">The job execution object.</span></span>

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

### <span data-ttu-id="31e68-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="31e68-137">-ParentResourceId</span></span>
<span data-ttu-id="31e68-138">Identyfikator zasobu wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="31e68-138">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e68-139">-ResourceGroupName</span></span>
<span data-ttu-id="31e68-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="31e68-140">The resource group name.</span></span>

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

### <span data-ttu-id="31e68-141">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="31e68-141">-ServerName</span></span>
<span data-ttu-id="31e68-142">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="31e68-142">The server name.</span></span>

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

### <span data-ttu-id="31e68-143">-Krokname</span><span class="sxs-lookup"><span data-stu-id="31e68-143">-StepName</span></span>
<span data-ttu-id="31e68-144">Nazwa etapu zadania.</span><span class="sxs-lookup"><span data-stu-id="31e68-144">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e68-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e68-145">CommonParameters</span></span>
<span data-ttu-id="31e68-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e68-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e68-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31e68-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e68-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31e68-148">INPUTS</span></span>

### <span data-ttu-id="31e68-149">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="31e68-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="31e68-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31e68-150">OUTPUTS</span></span>

### <span data-ttu-id="31e68-151">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="31e68-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="31e68-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31e68-152">NOTES</span></span>

## <span data-ttu-id="31e68-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31e68-153">RELATED LINKS</span></span>
