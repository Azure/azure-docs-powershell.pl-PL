---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 1279366f07ce071e223aea1f7cc048403b9b4379
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992370"
---
# <span data-ttu-id="8470b-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="8470b-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="8470b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8470b-102">SYNOPSIS</span></span>
<span data-ttu-id="8470b-103">Zatrzymuje zadanie, gdy jest ono identyfikatorem wykonywania zadania</span><span class="sxs-lookup"><span data-stu-id="8470b-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="8470b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8470b-104">SYNTAX</span></span>

### <span data-ttu-id="8470b-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="8470b-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8470b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8470b-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8470b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8470b-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8470b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8470b-108">DESCRIPTION</span></span>
<span data-ttu-id="8470b-109">Polecenie Stop-AzSqlElasticJob cmdlet zatrzymuje uruchomione wykonywanie zadania.</span><span class="sxs-lookup"><span data-stu-id="8470b-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="8470b-110">Zwraca bieżący stan wykonywania zadania.</span><span class="sxs-lookup"><span data-stu-id="8470b-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="8470b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8470b-111">EXAMPLES</span></span>

### <span data-ttu-id="8470b-112">Przykład 1. Zatrzymanie zadania z uruchomionym wykonaniem zadania</span><span class="sxs-lookup"><span data-stu-id="8470b-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="8470b-113">Zatrzymuje uruchamianie zadania i zwraca jego bieżący stan</span><span class="sxs-lookup"><span data-stu-id="8470b-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="8470b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8470b-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="8470b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8470b-115">PARAMETERS</span></span>

### <span data-ttu-id="8470b-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8470b-116">-AgentName</span></span>
<span data-ttu-id="8470b-117">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="8470b-117">The agent name</span></span>

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

### <span data-ttu-id="8470b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8470b-118">-DefaultProfile</span></span>
<span data-ttu-id="8470b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8470b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8470b-120">- JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="8470b-120">-JobExecutionId</span></span>
<span data-ttu-id="8470b-121">Identyfikator wykonywania zadania.</span><span class="sxs-lookup"><span data-stu-id="8470b-121">The job execution id.</span></span>

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

### <span data-ttu-id="8470b-122">— JobName</span><span class="sxs-lookup"><span data-stu-id="8470b-122">-JobName</span></span>
<span data-ttu-id="8470b-123">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="8470b-123">The job name</span></span>

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

### <span data-ttu-id="8470b-124">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="8470b-124">-ParentObject</span></span>
<span data-ttu-id="8470b-125">Obiekt bazy danych kontrolki agenta</span><span class="sxs-lookup"><span data-stu-id="8470b-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="8470b-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8470b-126">-ParentResourceId</span></span>
<span data-ttu-id="8470b-127">Identyfikator zasobu wykonywania zadań</span><span class="sxs-lookup"><span data-stu-id="8470b-127">The job execution resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8470b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8470b-128">-ResourceGroupName</span></span>
<span data-ttu-id="8470b-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8470b-129">The resource group name</span></span>

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

### <span data-ttu-id="8470b-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8470b-130">-ServerName</span></span>
<span data-ttu-id="8470b-131">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="8470b-131">The server name</span></span>

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

### <span data-ttu-id="8470b-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8470b-132">-Confirm</span></span>
<span data-ttu-id="8470b-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8470b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8470b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8470b-134">-WhatIf</span></span>
<span data-ttu-id="8470b-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8470b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8470b-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8470b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8470b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8470b-137">CommonParameters</span></span>
<span data-ttu-id="8470b-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8470b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8470b-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8470b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8470b-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8470b-140">INPUTS</span></span>

### <span data-ttu-id="8470b-141">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="8470b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="8470b-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8470b-142">OUTPUTS</span></span>

### <span data-ttu-id="8470b-143">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="8470b-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="8470b-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8470b-144">NOTES</span></span>

## <span data-ttu-id="8470b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8470b-145">RELATED LINKS</span></span>
