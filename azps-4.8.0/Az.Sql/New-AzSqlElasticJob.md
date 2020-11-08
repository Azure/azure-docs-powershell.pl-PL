---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063117"
---
# <span data-ttu-id="0ef5c-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="0ef5c-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="0ef5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ef5c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef5c-103">Tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="0ef5c-103">Creates a new job</span></span>

## <span data-ttu-id="0ef5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ef5c-104">SYNTAX</span></span>

### <span data-ttu-id="0ef5c-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0ef5c-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ef5c-106">Uruchomienia</span><span class="sxs-lookup"><span data-stu-id="0ef5c-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ef5c-107">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="0ef5c-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ef5c-108">Obiekt</span><span class="sxs-lookup"><span data-stu-id="0ef5c-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ef5c-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0ef5c-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ef5c-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0ef5c-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ef5c-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0ef5c-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ef5c-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0ef5c-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ef5c-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0ef5c-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ef5c-114">Opis</span><span class="sxs-lookup"><span data-stu-id="0ef5c-114">DESCRIPTION</span></span>
<span data-ttu-id="0ef5c-115">Polecenie cmdlet New-AzSqlElasticJob tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="0ef5c-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="0ef5c-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ef5c-116">EXAMPLES</span></span>

### <span data-ttu-id="0ef5c-117">Przykład 1. tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="0ef5c-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="0ef5c-118">Tworzy nowe zadanie</span><span class="sxs-lookup"><span data-stu-id="0ef5c-118">Creates a new job</span></span>

### <span data-ttu-id="0ef5c-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0ef5c-119">Example 2</span></span>

<span data-ttu-id="0ef5c-120">Tworzy nowe zadanie.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-120">Creates a new job.</span></span> <span data-ttu-id="0ef5c-121">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="0ef5c-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="0ef5c-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ef5c-122">PARAMETERS</span></span>

### <span data-ttu-id="0ef5c-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0ef5c-123">-AgentName</span></span>
<span data-ttu-id="0ef5c-124">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="0ef5c-124">The agent name</span></span>

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

### <span data-ttu-id="0ef5c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef5c-125">-DefaultProfile</span></span>
<span data-ttu-id="0ef5c-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ef5c-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="0ef5c-127">-Description</span></span>
<span data-ttu-id="0ef5c-128">Opis zadania</span><span class="sxs-lookup"><span data-stu-id="0ef5c-128">The job description</span></span>

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

### <span data-ttu-id="0ef5c-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="0ef5c-129">-Enable</span></span>
<span data-ttu-id="0ef5c-130">Flaga wskazująca, że klient chce włączyć to zadanie.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="0ef5c-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0ef5c-131">-EndTime</span></span>
<span data-ttu-id="0ef5c-132">Czas zakończenia harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="0ef5c-132">The job schedule end time</span></span>

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

### <span data-ttu-id="0ef5c-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="0ef5c-133">-IntervalCount</span></span>
<span data-ttu-id="0ef5c-134">Liczba interwałów harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="0ef5c-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="0ef5c-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="0ef5c-135">-IntervalType</span></span>
<span data-ttu-id="0ef5c-136">Typ interwału harmonogramu cyklicznego — może to być minuta, godzina, dzień, tydzień, miesiąc</span><span class="sxs-lookup"><span data-stu-id="0ef5c-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="0ef5c-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ef5c-137">-Name</span></span>
<span data-ttu-id="0ef5c-138">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="0ef5c-138">The job name</span></span>

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

### <span data-ttu-id="0ef5c-139">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="0ef5c-139">-ParentObject</span></span>
<span data-ttu-id="0ef5c-140">Obiekt wejściowy agenta</span><span class="sxs-lookup"><span data-stu-id="0ef5c-140">The agent input object</span></span>

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

### <span data-ttu-id="0ef5c-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0ef5c-141">-ParentResourceId</span></span>
<span data-ttu-id="0ef5c-142">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="0ef5c-142">The agent resource id</span></span>

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

### <span data-ttu-id="0ef5c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef5c-143">-ResourceGroupName</span></span>
<span data-ttu-id="0ef5c-144">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0ef5c-144">The resource group name</span></span>

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

### <span data-ttu-id="0ef5c-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="0ef5c-145">-RunOnce</span></span>
<span data-ttu-id="0ef5c-146">Flaga wskazująca zadanie zostanie uruchomiona raz</span><span class="sxs-lookup"><span data-stu-id="0ef5c-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="0ef5c-147">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0ef5c-147">-ServerName</span></span>
<span data-ttu-id="0ef5c-148">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="0ef5c-148">The server name</span></span>

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

### <span data-ttu-id="0ef5c-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0ef5c-149">-StartTime</span></span>
<span data-ttu-id="0ef5c-150">Czas rozpoczęcia planowania zadania</span><span class="sxs-lookup"><span data-stu-id="0ef5c-150">The job schedule start time</span></span>

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

### <span data-ttu-id="0ef5c-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ef5c-151">-Confirm</span></span>
<span data-ttu-id="0ef5c-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ef5c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef5c-153">-WhatIf</span></span>
<span data-ttu-id="0ef5c-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ef5c-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ef5c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef5c-156">CommonParameters</span></span>
<span data-ttu-id="0ef5c-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef5c-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ef5c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef5c-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ef5c-159">INPUTS</span></span>

### <span data-ttu-id="0ef5c-160">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="0ef5c-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="0ef5c-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ef5c-161">OUTPUTS</span></span>

### <span data-ttu-id="0ef5c-162">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="0ef5c-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="0ef5c-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ef5c-163">NOTES</span></span>

## <span data-ttu-id="0ef5c-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ef5c-164">RELATED LINKS</span></span>
