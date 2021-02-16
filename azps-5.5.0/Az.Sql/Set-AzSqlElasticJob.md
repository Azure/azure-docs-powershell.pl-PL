---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195978"
---
# <span data-ttu-id="50ee8-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="50ee8-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="50ee8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="50ee8-103">Aktualizacja zadania</span><span class="sxs-lookup"><span data-stu-id="50ee8-103">Updates a job</span></span>

## <span data-ttu-id="50ee8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50ee8-104">SYNTAX</span></span>

### <span data-ttu-id="50ee8-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="50ee8-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50ee8-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="50ee8-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50ee8-107">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="50ee8-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50ee8-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="50ee8-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50ee8-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="50ee8-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50ee8-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="50ee8-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50ee8-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="50ee8-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50ee8-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="50ee8-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50ee8-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="50ee8-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50ee8-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="50ee8-114">DESCRIPTION</span></span>
<span data-ttu-id="50ee8-115">Polecenie cmdlet Set-AzSqlElasticJob aktualizuje zadanie</span><span class="sxs-lookup"><span data-stu-id="50ee8-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="50ee8-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50ee8-116">EXAMPLES</span></span>

### <span data-ttu-id="50ee8-117">Przykład 1. Aktualizuje zadanie, aby rozpocząć godzinę od teraz i powtarzać je co 1 godzinę</span><span class="sxs-lookup"><span data-stu-id="50ee8-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="50ee8-118">Aktualizacja zadania</span><span class="sxs-lookup"><span data-stu-id="50ee8-118">Updates a job</span></span>

### <span data-ttu-id="50ee8-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="50ee8-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="50ee8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50ee8-120">PARAMETERS</span></span>

### <span data-ttu-id="50ee8-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="50ee8-121">-AgentName</span></span>
<span data-ttu-id="50ee8-122">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="50ee8-122">The agent name</span></span>

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

### <span data-ttu-id="50ee8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ee8-123">-DefaultProfile</span></span>
<span data-ttu-id="50ee8-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="50ee8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50ee8-125">— Opis</span><span class="sxs-lookup"><span data-stu-id="50ee8-125">-Description</span></span>
<span data-ttu-id="50ee8-126">Opis stanowiska</span><span class="sxs-lookup"><span data-stu-id="50ee8-126">The job description</span></span>

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

### <span data-ttu-id="50ee8-127">— Włącz</span><span class="sxs-lookup"><span data-stu-id="50ee8-127">-Enable</span></span>
<span data-ttu-id="50ee8-128">Flaga wskazująca, że klient chce włączyć to zadanie.</span><span class="sxs-lookup"><span data-stu-id="50ee8-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="50ee8-129">- EndTime</span><span class="sxs-lookup"><span data-stu-id="50ee8-129">-EndTime</span></span>
<span data-ttu-id="50ee8-130">Czas zakończenia harmonogramu zadania</span><span class="sxs-lookup"><span data-stu-id="50ee8-130">The job schedule end time</span></span>

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

### <span data-ttu-id="50ee8-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50ee8-131">-InputObject</span></span>
<span data-ttu-id="50ee8-132">Obiekt wprowadzania zadania</span><span class="sxs-lookup"><span data-stu-id="50ee8-132">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50ee8-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="50ee8-133">-IntervalCount</span></span>
<span data-ttu-id="50ee8-134">Liczba interwałów harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="50ee8-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="50ee8-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="50ee8-135">-IntervalType</span></span>
<span data-ttu-id="50ee8-136">Typ interwału harmonogramu cyklicznego — może to być minuta, godzina, dzień, tydzień, miesiąc</span><span class="sxs-lookup"><span data-stu-id="50ee8-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="50ee8-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="50ee8-137">-Name</span></span>
<span data-ttu-id="50ee8-138">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="50ee8-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ee8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50ee8-139">-ResourceGroupName</span></span>
<span data-ttu-id="50ee8-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="50ee8-140">The resource group name</span></span>

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

### <span data-ttu-id="50ee8-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50ee8-141">-ResourceId</span></span>
<span data-ttu-id="50ee8-142">Identyfikator zasobu zadań</span><span class="sxs-lookup"><span data-stu-id="50ee8-142">The job resource id</span></span>

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

### <span data-ttu-id="50ee8-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="50ee8-143">-RunOnce</span></span>
<span data-ttu-id="50ee8-144">Flaga wskazująca, że zadanie zostanie uruchomione raz</span><span class="sxs-lookup"><span data-stu-id="50ee8-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="50ee8-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="50ee8-145">-ServerName</span></span>
<span data-ttu-id="50ee8-146">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="50ee8-146">The server name</span></span>

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

### <span data-ttu-id="50ee8-147">— StartTime</span><span class="sxs-lookup"><span data-stu-id="50ee8-147">-StartTime</span></span>
<span data-ttu-id="50ee8-148">Czas rozpoczęcia harmonogramu zadania</span><span class="sxs-lookup"><span data-stu-id="50ee8-148">The job schedule start time</span></span>

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

### <span data-ttu-id="50ee8-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50ee8-149">-Confirm</span></span>
<span data-ttu-id="50ee8-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="50ee8-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50ee8-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50ee8-151">-WhatIf</span></span>
<span data-ttu-id="50ee8-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50ee8-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50ee8-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="50ee8-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50ee8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ee8-154">CommonParameters</span></span>
<span data-ttu-id="50ee8-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ee8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ee8-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50ee8-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ee8-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50ee8-157">INPUTS</span></span>

### <span data-ttu-id="50ee8-158">Microsoft.Azure.Commands.Sql.ElastycznaJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="50ee8-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="50ee8-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50ee8-159">OUTPUTS</span></span>

### <span data-ttu-id="50ee8-160">Microsoft.Azure.Commands.Sql.ElastycznaJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="50ee8-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="50ee8-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50ee8-161">NOTES</span></span>

## <span data-ttu-id="50ee8-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50ee8-162">RELATED LINKS</span></span>
