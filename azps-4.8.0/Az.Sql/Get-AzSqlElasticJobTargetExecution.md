---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 6e61a83d843e0ceaa7d7926060da848d80d16eae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222231"
---
# <span data-ttu-id="9cbc3-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="9cbc3-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="9cbc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbc3-103">Pobiera co najmniej jedno wykonanie zadania w celu</span><span class="sxs-lookup"><span data-stu-id="9cbc3-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="9cbc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cbc3-104">SYNTAX</span></span>

### <span data-ttu-id="9cbc3-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9cbc3-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cbc3-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="9cbc3-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cbc3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9cbc3-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cbc3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9cbc3-108">DESCRIPTION</span></span>
<span data-ttu-id="9cbc3-109">Polecenie cmdlet Get-AzSqlElasticJobTargetExecution umożliwia pobieranie co najmniej jednego wykonania zadania w celu wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="9cbc3-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="9cbc3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cbc3-110">EXAMPLES</span></span>

### <span data-ttu-id="9cbc3-111">Przykład 1: umożliwia odprowadzenie co najmniej jednego wykonania zadania w celu wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="9cbc3-111">Example 1: Gets one or more job target executions from a job executions</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="9cbc3-112">Przykład 2: Pobiera co najmniej jedno wykonanie zadania docelowego z wykonania zadania — filtrowanie według nazwy kroku</span><span class="sxs-lookup"><span data-stu-id="9cbc3-112">Example 2: Gets one or more job target executions from a job executions - filtering by step name</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="9cbc3-113">Pobiera co najmniej jedno wykonanie zadania w celu</span><span class="sxs-lookup"><span data-stu-id="9cbc3-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="9cbc3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cbc3-114">PARAMETERS</span></span>

### <span data-ttu-id="9cbc3-115">— Aktywne</span><span class="sxs-lookup"><span data-stu-id="9cbc3-115">-Active</span></span>
<span data-ttu-id="9cbc3-116">Flaga filtrowania według aktywnych operacji.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-116">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="9cbc3-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9cbc3-117">-AgentName</span></span>
<span data-ttu-id="9cbc3-118">Nazwa agenta.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-118">The agent name.</span></span>

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

### <span data-ttu-id="9cbc3-119">-Count</span><span class="sxs-lookup"><span data-stu-id="9cbc3-119">-Count</span></span>
<span data-ttu-id="9cbc3-120">Funkcja count zwraca liczbę pierwszych wykonań.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-120">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="9cbc3-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="9cbc3-121">-CreateTimeMax</span></span>
<span data-ttu-id="9cbc3-122">Filtruj według — Utwórz maks. czas</span><span class="sxs-lookup"><span data-stu-id="9cbc3-122">Filter by create time max</span></span>

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

### <span data-ttu-id="9cbc3-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="9cbc3-123">-CreateTimeMin</span></span>
<span data-ttu-id="9cbc3-124">Filtrowanie według, min. czas</span><span class="sxs-lookup"><span data-stu-id="9cbc3-124">Filter by create time min</span></span>

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

### <span data-ttu-id="9cbc3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbc3-125">-DefaultProfile</span></span>
<span data-ttu-id="9cbc3-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cbc3-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="9cbc3-127">-EndTimeMax</span></span>
<span data-ttu-id="9cbc3-128">Filtruj według godziny zakończenia, maks.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-128">Filter by end time max.</span></span>

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

### <span data-ttu-id="9cbc3-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="9cbc3-129">-EndTimeMin</span></span>
<span data-ttu-id="9cbc3-130">Filtruj według godziny zakończenia, min.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-130">Filter by end time min.</span></span>

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

### <span data-ttu-id="9cbc3-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="9cbc3-131">-JobExecutionId</span></span>
<span data-ttu-id="9cbc3-132">Identyfikator wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-132">The job execution id.</span></span>

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

### <span data-ttu-id="9cbc3-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="9cbc3-133">-JobName</span></span>
<span data-ttu-id="9cbc3-134">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-134">The job name.</span></span>

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

### <span data-ttu-id="9cbc3-135">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="9cbc3-135">-ParentObject</span></span>
<span data-ttu-id="9cbc3-136">Obiekt wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-136">The job execution object.</span></span>

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

### <span data-ttu-id="9cbc3-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9cbc3-137">-ParentResourceId</span></span>
<span data-ttu-id="9cbc3-138">Identyfikator zasobu wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-138">The job execution resource id.</span></span>

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

### <span data-ttu-id="9cbc3-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cbc3-139">-ResourceGroupName</span></span>
<span data-ttu-id="9cbc3-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-140">The resource group name.</span></span>

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

### <span data-ttu-id="9cbc3-141">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="9cbc3-141">-ServerName</span></span>
<span data-ttu-id="9cbc3-142">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-142">The server name.</span></span>

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

### <span data-ttu-id="9cbc3-143">-Krokname</span><span class="sxs-lookup"><span data-stu-id="9cbc3-143">-StepName</span></span>
<span data-ttu-id="9cbc3-144">Nazwa etapu zadania.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-144">The job step name.</span></span>

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

### <span data-ttu-id="9cbc3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbc3-145">CommonParameters</span></span>
<span data-ttu-id="9cbc3-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbc3-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cbc3-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbc3-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cbc3-148">INPUTS</span></span>

### <span data-ttu-id="9cbc3-149">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="9cbc3-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="9cbc3-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cbc3-150">OUTPUTS</span></span>

### <span data-ttu-id="9cbc3-151">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="9cbc3-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="9cbc3-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cbc3-152">NOTES</span></span>

## <span data-ttu-id="9cbc3-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cbc3-153">RELATED LINKS</span></span>
