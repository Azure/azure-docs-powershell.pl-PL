---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234061"
---
# <span data-ttu-id="fd9d6-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="fd9d6-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="fd9d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9d6-103">Aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="fd9d6-103">Updates a job</span></span>

## <span data-ttu-id="fd9d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd9d6-104">SYNTAX</span></span>

### <span data-ttu-id="fd9d6-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fd9d6-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd9d6-106">Uruchomienia</span><span class="sxs-lookup"><span data-stu-id="fd9d6-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd9d6-107">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="fd9d6-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd9d6-108">Obiekt</span><span class="sxs-lookup"><span data-stu-id="fd9d6-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd9d6-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fd9d6-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd9d6-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fd9d6-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd9d6-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd9d6-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd9d6-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fd9d6-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd9d6-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fd9d6-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd9d6-114">Opis</span><span class="sxs-lookup"><span data-stu-id="fd9d6-114">DESCRIPTION</span></span>
<span data-ttu-id="fd9d6-115">Polecenie cmdlet Set-AzSqlElasticJob aktualizuje zadanie</span><span class="sxs-lookup"><span data-stu-id="fd9d6-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="fd9d6-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd9d6-116">EXAMPLES</span></span>

### <span data-ttu-id="fd9d6-117">Przykład 1: umożliwia zaktualizowanie zadania w celu rozpoczęcia od razu godziny i powtarzanie co 1 godzinę</span><span class="sxs-lookup"><span data-stu-id="fd9d6-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="fd9d6-118">Aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="fd9d6-118">Updates a job</span></span>

### <span data-ttu-id="fd9d6-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fd9d6-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="fd9d6-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd9d6-120">PARAMETERS</span></span>

### <span data-ttu-id="fd9d6-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fd9d6-121">-AgentName</span></span>
<span data-ttu-id="fd9d6-122">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="fd9d6-122">The agent name</span></span>

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

### <span data-ttu-id="fd9d6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9d6-123">-DefaultProfile</span></span>
<span data-ttu-id="fd9d6-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd9d6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd9d6-125">— Opis</span><span class="sxs-lookup"><span data-stu-id="fd9d6-125">-Description</span></span>
<span data-ttu-id="fd9d6-126">Opis zadania</span><span class="sxs-lookup"><span data-stu-id="fd9d6-126">The job description</span></span>

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

### <span data-ttu-id="fd9d6-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="fd9d6-127">-Enable</span></span>
<span data-ttu-id="fd9d6-128">Flaga wskazująca, że klient chce włączyć to zadanie.</span><span class="sxs-lookup"><span data-stu-id="fd9d6-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="fd9d6-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="fd9d6-129">-EndTime</span></span>
<span data-ttu-id="fd9d6-130">Czas zakończenia harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="fd9d6-130">The job schedule end time</span></span>

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

### <span data-ttu-id="fd9d6-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fd9d6-131">-InputObject</span></span>
<span data-ttu-id="fd9d6-132">Obiekt wejściowy zlecenia</span><span class="sxs-lookup"><span data-stu-id="fd9d6-132">The job input object</span></span>

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

### <span data-ttu-id="fd9d6-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="fd9d6-133">-IntervalCount</span></span>
<span data-ttu-id="fd9d6-134">Liczba interwałów harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="fd9d6-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="fd9d6-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="fd9d6-135">-IntervalType</span></span>
<span data-ttu-id="fd9d6-136">Typ interwału harmonogramu cyklicznego — może to być minuta, godzina, dzień, tydzień, miesiąc</span><span class="sxs-lookup"><span data-stu-id="fd9d6-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="fd9d6-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd9d6-137">-Name</span></span>
<span data-ttu-id="fd9d6-138">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="fd9d6-138">The job name</span></span>

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

### <span data-ttu-id="fd9d6-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd9d6-139">-ResourceGroupName</span></span>
<span data-ttu-id="fd9d6-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fd9d6-140">The resource group name</span></span>

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

### <span data-ttu-id="fd9d6-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd9d6-141">-ResourceId</span></span>
<span data-ttu-id="fd9d6-142">Identyfikator zasobu zadania</span><span class="sxs-lookup"><span data-stu-id="fd9d6-142">The job resource id</span></span>

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

### <span data-ttu-id="fd9d6-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="fd9d6-143">-RunOnce</span></span>
<span data-ttu-id="fd9d6-144">Flaga wskazująca zadanie zostanie uruchomiona raz</span><span class="sxs-lookup"><span data-stu-id="fd9d6-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="fd9d6-145">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fd9d6-145">-ServerName</span></span>
<span data-ttu-id="fd9d6-146">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="fd9d6-146">The server name</span></span>

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

### <span data-ttu-id="fd9d6-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fd9d6-147">-StartTime</span></span>
<span data-ttu-id="fd9d6-148">Czas rozpoczęcia planowania zadania</span><span class="sxs-lookup"><span data-stu-id="fd9d6-148">The job schedule start time</span></span>

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

### <span data-ttu-id="fd9d6-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd9d6-149">-Confirm</span></span>
<span data-ttu-id="fd9d6-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd9d6-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd9d6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd9d6-151">-WhatIf</span></span>
<span data-ttu-id="fd9d6-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd9d6-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd9d6-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd9d6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd9d6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9d6-154">CommonParameters</span></span>
<span data-ttu-id="fd9d6-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd9d6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9d6-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd9d6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9d6-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd9d6-157">INPUTS</span></span>

### <span data-ttu-id="fd9d6-158">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="fd9d6-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="fd9d6-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd9d6-159">OUTPUTS</span></span>

### <span data-ttu-id="fd9d6-160">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="fd9d6-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="fd9d6-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd9d6-161">NOTES</span></span>

## <span data-ttu-id="fd9d6-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd9d6-162">RELATED LINKS</span></span>
