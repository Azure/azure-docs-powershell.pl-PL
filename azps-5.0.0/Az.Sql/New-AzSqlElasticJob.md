---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225651"
---
# <span data-ttu-id="35127-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="35127-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="35127-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35127-102">SYNOPSIS</span></span>
<span data-ttu-id="35127-103">Tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="35127-103">Creates a new job</span></span>

## <span data-ttu-id="35127-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35127-104">SYNTAX</span></span>

### <span data-ttu-id="35127-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35127-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35127-106">Uruchomienia</span><span class="sxs-lookup"><span data-stu-id="35127-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35127-107">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="35127-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35127-108">Obiekt</span><span class="sxs-lookup"><span data-stu-id="35127-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35127-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="35127-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35127-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="35127-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35127-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="35127-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35127-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="35127-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35127-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="35127-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35127-114">Opis</span><span class="sxs-lookup"><span data-stu-id="35127-114">DESCRIPTION</span></span>
<span data-ttu-id="35127-115">Polecenie cmdlet New-AzSqlElasticJob tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="35127-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="35127-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35127-116">EXAMPLES</span></span>

### <span data-ttu-id="35127-117">Przykład 1. tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="35127-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="35127-118">Tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="35127-118">Creates a new job</span></span>

### <span data-ttu-id="35127-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="35127-119">Example 2</span></span>

<span data-ttu-id="35127-120">Tworzy nowe zadanie.</span><span class="sxs-lookup"><span data-stu-id="35127-120">Creates a new job.</span></span> <span data-ttu-id="35127-121">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="35127-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="35127-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35127-122">PARAMETERS</span></span>

### <span data-ttu-id="35127-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="35127-123">-AgentName</span></span>
<span data-ttu-id="35127-124">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="35127-124">The agent name</span></span>

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

### <span data-ttu-id="35127-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35127-125">-DefaultProfile</span></span>
<span data-ttu-id="35127-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35127-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35127-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="35127-127">-Description</span></span>
<span data-ttu-id="35127-128">Opis zadania</span><span class="sxs-lookup"><span data-stu-id="35127-128">The job description</span></span>

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

### <span data-ttu-id="35127-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="35127-129">-Enable</span></span>
<span data-ttu-id="35127-130">Flaga wskazująca, że klient chce włączyć to zadanie.</span><span class="sxs-lookup"><span data-stu-id="35127-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="35127-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="35127-131">-EndTime</span></span>
<span data-ttu-id="35127-132">Czas zakończenia harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="35127-132">The job schedule end time</span></span>

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

### <span data-ttu-id="35127-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="35127-133">-IntervalCount</span></span>
<span data-ttu-id="35127-134">Liczba interwałów harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="35127-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="35127-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="35127-135">-IntervalType</span></span>
<span data-ttu-id="35127-136">Typ interwału harmonogramu cyklicznego — może to być minuta, godzina, dzień, tydzień, miesiąc</span><span class="sxs-lookup"><span data-stu-id="35127-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="35127-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="35127-137">-Name</span></span>
<span data-ttu-id="35127-138">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="35127-138">The job name</span></span>

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

### <span data-ttu-id="35127-139">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="35127-139">-ParentObject</span></span>
<span data-ttu-id="35127-140">Obiekt wejściowy agenta</span><span class="sxs-lookup"><span data-stu-id="35127-140">The agent input object</span></span>

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

### <span data-ttu-id="35127-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="35127-141">-ParentResourceId</span></span>
<span data-ttu-id="35127-142">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="35127-142">The agent resource id</span></span>

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

### <span data-ttu-id="35127-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35127-143">-ResourceGroupName</span></span>
<span data-ttu-id="35127-144">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="35127-144">The resource group name</span></span>

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

### <span data-ttu-id="35127-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="35127-145">-RunOnce</span></span>
<span data-ttu-id="35127-146">Flaga wskazująca zadanie zostanie uruchomiona raz</span><span class="sxs-lookup"><span data-stu-id="35127-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="35127-147">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="35127-147">-ServerName</span></span>
<span data-ttu-id="35127-148">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="35127-148">The server name</span></span>

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

### <span data-ttu-id="35127-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="35127-149">-StartTime</span></span>
<span data-ttu-id="35127-150">Czas rozpoczęcia planowania zadania</span><span class="sxs-lookup"><span data-stu-id="35127-150">The job schedule start time</span></span>

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

### <span data-ttu-id="35127-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35127-151">-Confirm</span></span>
<span data-ttu-id="35127-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35127-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35127-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35127-153">-WhatIf</span></span>
<span data-ttu-id="35127-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35127-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35127-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35127-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35127-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35127-156">CommonParameters</span></span>
<span data-ttu-id="35127-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35127-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35127-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35127-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35127-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35127-159">INPUTS</span></span>

### <span data-ttu-id="35127-160">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="35127-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="35127-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35127-161">OUTPUTS</span></span>

### <span data-ttu-id="35127-162">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="35127-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="35127-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35127-163">NOTES</span></span>

## <span data-ttu-id="35127-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35127-164">RELATED LINKS</span></span>
