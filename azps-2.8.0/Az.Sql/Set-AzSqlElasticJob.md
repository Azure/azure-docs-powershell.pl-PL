---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 04f182cb410e77a9ca61aa6f80da14c08e517406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887129"
---
# <span data-ttu-id="a37a9-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="a37a9-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="a37a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a37a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a37a9-103">Aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="a37a9-103">Updates a job</span></span>

## <span data-ttu-id="a37a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a37a9-104">SYNTAX</span></span>

### <span data-ttu-id="a37a9-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a37a9-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37a9-106">Uruchomienia</span><span class="sxs-lookup"><span data-stu-id="a37a9-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37a9-107">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="a37a9-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37a9-108">Obiekt</span><span class="sxs-lookup"><span data-stu-id="a37a9-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a37a9-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="a37a9-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37a9-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="a37a9-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37a9-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a37a9-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37a9-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a37a9-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37a9-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a37a9-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a37a9-114">Opis</span><span class="sxs-lookup"><span data-stu-id="a37a9-114">DESCRIPTION</span></span>
<span data-ttu-id="a37a9-115">Polecenie cmdlet Set-AzSqlElasticJob aktualizuje zadanie</span><span class="sxs-lookup"><span data-stu-id="a37a9-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="a37a9-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a37a9-116">EXAMPLES</span></span>

### <span data-ttu-id="a37a9-117">Przykład 1-umożliwia zaktualizowanie zadania w celu rozpoczęcia od razu godziny i powtarzanie co 1 godzinę</span><span class="sxs-lookup"><span data-stu-id="a37a9-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="a37a9-118">Aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="a37a9-118">Updates a job</span></span>

## <span data-ttu-id="a37a9-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a37a9-119">PARAMETERS</span></span>

### <span data-ttu-id="a37a9-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a37a9-120">-AgentName</span></span>
<span data-ttu-id="a37a9-121">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="a37a9-121">The agent name</span></span>

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

### <span data-ttu-id="a37a9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a37a9-122">-DefaultProfile</span></span>
<span data-ttu-id="a37a9-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a37a9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a37a9-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="a37a9-124">-Description</span></span>
<span data-ttu-id="a37a9-125">Opis zadania</span><span class="sxs-lookup"><span data-stu-id="a37a9-125">The job description</span></span>

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

### <span data-ttu-id="a37a9-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="a37a9-126">-Enable</span></span>
<span data-ttu-id="a37a9-127">Flaga wskazująca, że klient chce włączyć to zadanie.</span><span class="sxs-lookup"><span data-stu-id="a37a9-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="a37a9-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a37a9-128">-EndTime</span></span>
<span data-ttu-id="a37a9-129">Czas zakończenia harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="a37a9-129">The job schedule end time</span></span>

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

### <span data-ttu-id="a37a9-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a37a9-130">-InputObject</span></span>
<span data-ttu-id="a37a9-131">Obiekt wejściowy zlecenia</span><span class="sxs-lookup"><span data-stu-id="a37a9-131">The job input object</span></span>

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

### <span data-ttu-id="a37a9-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="a37a9-132">-IntervalCount</span></span>
<span data-ttu-id="a37a9-133">Liczba interwałów harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="a37a9-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="a37a9-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="a37a9-134">-IntervalType</span></span>
<span data-ttu-id="a37a9-135">Typ interwału harmonogramu cyklicznego — może to być minuta, godzina, dzień, tydzień, miesiąc</span><span class="sxs-lookup"><span data-stu-id="a37a9-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="a37a9-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a37a9-136">-Name</span></span>
<span data-ttu-id="a37a9-137">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="a37a9-137">The job name</span></span>

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

### <span data-ttu-id="a37a9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a37a9-138">-ResourceGroupName</span></span>
<span data-ttu-id="a37a9-139">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a37a9-139">The resource group name</span></span>

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

### <span data-ttu-id="a37a9-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a37a9-140">-ResourceId</span></span>
<span data-ttu-id="a37a9-141">Identyfikator zasobu zadania</span><span class="sxs-lookup"><span data-stu-id="a37a9-141">The job resource id</span></span>

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

### <span data-ttu-id="a37a9-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="a37a9-142">-RunOnce</span></span>
<span data-ttu-id="a37a9-143">Flaga wskazująca zadanie zostanie uruchomiona raz</span><span class="sxs-lookup"><span data-stu-id="a37a9-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="a37a9-144">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a37a9-144">-ServerName</span></span>
<span data-ttu-id="a37a9-145">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="a37a9-145">The server name</span></span>

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

### <span data-ttu-id="a37a9-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a37a9-146">-StartTime</span></span>
<span data-ttu-id="a37a9-147">Czas rozpoczęcia planowania zadania</span><span class="sxs-lookup"><span data-stu-id="a37a9-147">The job schedule start time</span></span>

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

### <span data-ttu-id="a37a9-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a37a9-148">-Confirm</span></span>
<span data-ttu-id="a37a9-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a37a9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a37a9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a37a9-150">-WhatIf</span></span>
<span data-ttu-id="a37a9-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a37a9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a37a9-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a37a9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a37a9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a37a9-153">CommonParameters</span></span>
<span data-ttu-id="a37a9-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a37a9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a37a9-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a37a9-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a37a9-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a37a9-156">INPUTS</span></span>

### <span data-ttu-id="a37a9-157">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="a37a9-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="a37a9-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a37a9-158">OUTPUTS</span></span>

### <span data-ttu-id="a37a9-159">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="a37a9-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="a37a9-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a37a9-160">NOTES</span></span>

## <span data-ttu-id="a37a9-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a37a9-161">RELATED LINKS</span></span>
