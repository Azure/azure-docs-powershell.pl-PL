---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 961f37db94cff87952b2811a528a94cc71ffabff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010161"
---
# <span data-ttu-id="dc168-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="dc168-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="dc168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc168-102">SYNOPSIS</span></span>
<span data-ttu-id="dc168-103">Tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="dc168-103">Creates a new job</span></span>

## <span data-ttu-id="dc168-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dc168-104">SYNTAX</span></span>

### <span data-ttu-id="dc168-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="dc168-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc168-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="dc168-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc168-107">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="dc168-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc168-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc168-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc168-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="dc168-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc168-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="dc168-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc168-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dc168-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc168-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dc168-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc168-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dc168-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc168-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="dc168-114">DESCRIPTION</span></span>
<span data-ttu-id="dc168-115">Polecenie New-AzSqlElasticJob cmdlet tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="dc168-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="dc168-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dc168-116">EXAMPLES</span></span>

### <span data-ttu-id="dc168-117">Przykład 1. Tworzenie nowego zadania</span><span class="sxs-lookup"><span data-stu-id="dc168-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="dc168-118">Tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="dc168-118">Creates a new job</span></span>

### <span data-ttu-id="dc168-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dc168-119">Example 2</span></span>

<span data-ttu-id="dc168-120">Tworzy nowe zadanie.</span><span class="sxs-lookup"><span data-stu-id="dc168-120">Creates a new job.</span></span> <span data-ttu-id="dc168-121">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="dc168-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="dc168-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc168-122">PARAMETERS</span></span>

### <span data-ttu-id="dc168-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="dc168-123">-AgentName</span></span>
<span data-ttu-id="dc168-124">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="dc168-124">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc168-125">-DefaultProfile</span></span>
<span data-ttu-id="dc168-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc168-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc168-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="dc168-127">-Description</span></span>
<span data-ttu-id="dc168-128">Opis stanowiska</span><span class="sxs-lookup"><span data-stu-id="dc168-128">The job description</span></span>

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

### <span data-ttu-id="dc168-129">— Włącz</span><span class="sxs-lookup"><span data-stu-id="dc168-129">-Enable</span></span>
<span data-ttu-id="dc168-130">Flaga wskazująca, że klient chce włączyć to zadanie.</span><span class="sxs-lookup"><span data-stu-id="dc168-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="dc168-131">- EndTime</span><span class="sxs-lookup"><span data-stu-id="dc168-131">-EndTime</span></span>
<span data-ttu-id="dc168-132">Czas zakończenia harmonogramu zadania</span><span class="sxs-lookup"><span data-stu-id="dc168-132">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="dc168-133">-IntervalCount</span></span>
<span data-ttu-id="dc168-134">Liczba interwałów harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="dc168-134">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="dc168-135">-IntervalType</span></span>
<span data-ttu-id="dc168-136">Typ interwału harmonogramu cyklicznego — może to być minuta, godzina, dzień, tydzień, miesiąc</span><span class="sxs-lookup"><span data-stu-id="dc168-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dc168-137">-Name</span></span>
<span data-ttu-id="dc168-138">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="dc168-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-139">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="dc168-139">-ParentObject</span></span>
<span data-ttu-id="dc168-140">Obiekt wejściowy agenta</span><span class="sxs-lookup"><span data-stu-id="dc168-140">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dc168-141">-ParentResourceId</span></span>
<span data-ttu-id="dc168-142">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="dc168-142">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc168-143">-ResourceGroupName</span></span>
<span data-ttu-id="dc168-144">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dc168-144">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="dc168-145">-RunOnce</span></span>
<span data-ttu-id="dc168-146">Flaga wskazująca, że zadanie zostanie uruchomione raz</span><span class="sxs-lookup"><span data-stu-id="dc168-146">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dc168-147">-ServerName</span></span>
<span data-ttu-id="dc168-148">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="dc168-148">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-149">— StartTime</span><span class="sxs-lookup"><span data-stu-id="dc168-149">-StartTime</span></span>
<span data-ttu-id="dc168-150">Czas rozpoczęcia harmonogramu zadania</span><span class="sxs-lookup"><span data-stu-id="dc168-150">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc168-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc168-151">-Confirm</span></span>
<span data-ttu-id="dc168-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dc168-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc168-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc168-153">-WhatIf</span></span>
<span data-ttu-id="dc168-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc168-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc168-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dc168-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc168-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc168-156">CommonParameters</span></span>
<span data-ttu-id="dc168-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc168-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc168-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc168-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc168-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc168-159">INPUTS</span></span>

### <span data-ttu-id="dc168-160">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="dc168-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="dc168-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc168-161">OUTPUTS</span></span>

### <span data-ttu-id="dc168-162">Microsoft.Azure.Commands.Sql.ElastycznaJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="dc168-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="dc168-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dc168-163">NOTES</span></span>

## <span data-ttu-id="dc168-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc168-164">RELATED LINKS</span></span>
