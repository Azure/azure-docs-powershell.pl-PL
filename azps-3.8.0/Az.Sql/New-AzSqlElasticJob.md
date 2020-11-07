---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 98c019c8dedf767fc2b75bb2133f7c545ffd03ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894541"
---
# <span data-ttu-id="4f5c6-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="4f5c6-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="4f5c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5c6-103">Tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="4f5c6-103">Creates a new job</span></span>

## <span data-ttu-id="4f5c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f5c6-104">SYNTAX</span></span>

### <span data-ttu-id="4f5c6-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4f5c6-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f5c6-106">Uruchomienia</span><span class="sxs-lookup"><span data-stu-id="4f5c6-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f5c6-107">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="4f5c6-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f5c6-108">Obiekt</span><span class="sxs-lookup"><span data-stu-id="4f5c6-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f5c6-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4f5c6-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f5c6-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4f5c6-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f5c6-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4f5c6-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f5c6-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4f5c6-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f5c6-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4f5c6-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f5c6-114">Opis</span><span class="sxs-lookup"><span data-stu-id="4f5c6-114">DESCRIPTION</span></span>
<span data-ttu-id="4f5c6-115">Polecenie cmdlet New-AzSqlElasticJob tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="4f5c6-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="4f5c6-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f5c6-116">EXAMPLES</span></span>

### <span data-ttu-id="4f5c6-117">Przykład 1-tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="4f5c6-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="4f5c6-118">Tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="4f5c6-118">Creates a new job</span></span>

## <span data-ttu-id="4f5c6-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f5c6-119">PARAMETERS</span></span>

### <span data-ttu-id="4f5c6-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4f5c6-120">-AgentName</span></span>
<span data-ttu-id="4f5c6-121">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="4f5c6-121">The agent name</span></span>

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

### <span data-ttu-id="4f5c6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5c6-122">-DefaultProfile</span></span>
<span data-ttu-id="4f5c6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f5c6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f5c6-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="4f5c6-124">-Description</span></span>
<span data-ttu-id="4f5c6-125">Opis zadania</span><span class="sxs-lookup"><span data-stu-id="4f5c6-125">The job description</span></span>

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

### <span data-ttu-id="4f5c6-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="4f5c6-126">-Enable</span></span>
<span data-ttu-id="4f5c6-127">Flaga wskazująca, że klient chce włączyć to zadanie.</span><span class="sxs-lookup"><span data-stu-id="4f5c6-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="4f5c6-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4f5c6-128">-EndTime</span></span>
<span data-ttu-id="4f5c6-129">Czas zakończenia harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="4f5c6-129">The job schedule end time</span></span>

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

### <span data-ttu-id="4f5c6-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="4f5c6-130">-IntervalCount</span></span>
<span data-ttu-id="4f5c6-131">Liczba interwałów harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="4f5c6-131">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="4f5c6-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="4f5c6-132">-IntervalType</span></span>
<span data-ttu-id="4f5c6-133">Typ interwału harmonogramu cyklicznego — może to być minuta, godzina, dzień, tydzień, miesiąc</span><span class="sxs-lookup"><span data-stu-id="4f5c6-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="4f5c6-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4f5c6-134">-Name</span></span>
<span data-ttu-id="4f5c6-135">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="4f5c6-135">The job name</span></span>

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

### <span data-ttu-id="4f5c6-136">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="4f5c6-136">-ParentObject</span></span>
<span data-ttu-id="4f5c6-137">Obiekt wejściowy agenta</span><span class="sxs-lookup"><span data-stu-id="4f5c6-137">The agent input object</span></span>

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

### <span data-ttu-id="4f5c6-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4f5c6-138">-ParentResourceId</span></span>
<span data-ttu-id="4f5c6-139">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="4f5c6-139">The agent resource id</span></span>

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

### <span data-ttu-id="4f5c6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f5c6-140">-ResourceGroupName</span></span>
<span data-ttu-id="4f5c6-141">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4f5c6-141">The resource group name</span></span>

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

### <span data-ttu-id="4f5c6-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="4f5c6-142">-RunOnce</span></span>
<span data-ttu-id="4f5c6-143">Flaga wskazująca zadanie zostanie uruchomiona raz</span><span class="sxs-lookup"><span data-stu-id="4f5c6-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="4f5c6-144">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4f5c6-144">-ServerName</span></span>
<span data-ttu-id="4f5c6-145">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="4f5c6-145">The server name</span></span>

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

### <span data-ttu-id="4f5c6-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4f5c6-146">-StartTime</span></span>
<span data-ttu-id="4f5c6-147">Czas rozpoczęcia planowania zadania</span><span class="sxs-lookup"><span data-stu-id="4f5c6-147">The job schedule start time</span></span>

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

### <span data-ttu-id="4f5c6-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4f5c6-148">-Confirm</span></span>
<span data-ttu-id="4f5c6-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f5c6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f5c6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f5c6-150">-WhatIf</span></span>
<span data-ttu-id="4f5c6-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f5c6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f5c6-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4f5c6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f5c6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5c6-153">CommonParameters</span></span>
<span data-ttu-id="4f5c6-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f5c6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5c6-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f5c6-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5c6-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f5c6-156">INPUTS</span></span>

### <span data-ttu-id="4f5c6-157">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="4f5c6-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="4f5c6-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f5c6-158">OUTPUTS</span></span>

### <span data-ttu-id="4f5c6-159">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="4f5c6-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="4f5c6-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f5c6-160">NOTES</span></span>

## <span data-ttu-id="4f5c6-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f5c6-161">RELATED LINKS</span></span>
