---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195914"
---
# <span data-ttu-id="8428b-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="8428b-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="8428b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8428b-102">SYNOPSIS</span></span>
<span data-ttu-id="8428b-103">Rozpoczyna zadanie, zwracając identyfikator wykonywania zadania, który można ankietować w celu wyświetlenia jego stanu</span><span class="sxs-lookup"><span data-stu-id="8428b-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="8428b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8428b-104">SYNTAX</span></span>

### <span data-ttu-id="8428b-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="8428b-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8428b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8428b-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8428b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8428b-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8428b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8428b-108">DESCRIPTION</span></span>
<span data-ttu-id="8428b-109">Polecenie Start-AzSqlElasticJob uruchamia zadanie zwracające nowe wykonywanie zadania</span><span class="sxs-lookup"><span data-stu-id="8428b-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="8428b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8428b-110">EXAMPLES</span></span>

### <span data-ttu-id="8428b-111">Przykład 1. Rozpoczynanie zadania zwracające nowe wykonywanie zadania</span><span class="sxs-lookup"><span data-stu-id="8428b-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="8428b-112">Rozpoczynanie zadania zwracające nowe wykonywanie zadania</span><span class="sxs-lookup"><span data-stu-id="8428b-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="8428b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8428b-113">PARAMETERS</span></span>

### <span data-ttu-id="8428b-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8428b-114">-AgentName</span></span>
<span data-ttu-id="8428b-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="8428b-115">The agent name</span></span>

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

### <span data-ttu-id="8428b-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8428b-116">-AsJob</span></span>
<span data-ttu-id="8428b-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8428b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8428b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8428b-118">-DefaultProfile</span></span>
<span data-ttu-id="8428b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8428b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8428b-120">— JobName</span><span class="sxs-lookup"><span data-stu-id="8428b-120">-JobName</span></span>
<span data-ttu-id="8428b-121">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="8428b-121">The job name</span></span>

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

### <span data-ttu-id="8428b-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="8428b-122">-ParentObject</span></span>
<span data-ttu-id="8428b-123">Obiekt zadania</span><span class="sxs-lookup"><span data-stu-id="8428b-123">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8428b-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8428b-124">-ParentResourceId</span></span>
<span data-ttu-id="8428b-125">Identyfikator zasobu zadań</span><span class="sxs-lookup"><span data-stu-id="8428b-125">The job resource id</span></span>

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

### <span data-ttu-id="8428b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8428b-126">-ResourceGroupName</span></span>
<span data-ttu-id="8428b-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8428b-127">The resource group name</span></span>

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

### <span data-ttu-id="8428b-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8428b-128">-ServerName</span></span>
<span data-ttu-id="8428b-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="8428b-129">The server name</span></span>

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

### <span data-ttu-id="8428b-130">— Czekanie</span><span class="sxs-lookup"><span data-stu-id="8428b-130">-Wait</span></span>
<span data-ttu-id="8428b-131">Flaga oczekiwania wskazująca oczekiwanie na wykonanie zadania</span><span class="sxs-lookup"><span data-stu-id="8428b-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="8428b-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8428b-132">-Confirm</span></span>
<span data-ttu-id="8428b-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8428b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8428b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8428b-134">-WhatIf</span></span>
<span data-ttu-id="8428b-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8428b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8428b-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8428b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8428b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8428b-137">CommonParameters</span></span>
<span data-ttu-id="8428b-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8428b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8428b-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8428b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8428b-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8428b-140">INPUTS</span></span>

### <span data-ttu-id="8428b-141">Microsoft.Azure.Commands.Sql.ElastycznaJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="8428b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="8428b-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8428b-142">OUTPUTS</span></span>

### <span data-ttu-id="8428b-143">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="8428b-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="8428b-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8428b-144">NOTES</span></span>

## <span data-ttu-id="8428b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8428b-145">RELATED LINKS</span></span>
