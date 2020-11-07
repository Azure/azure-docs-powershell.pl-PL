---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895686"
---
# <span data-ttu-id="78d3c-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="78d3c-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="78d3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="78d3c-103">Rozpoczyna zadanie, zwracając identyfikator wykonywania zadania, który może być sondowany w celu wyświetlenia jego statusu.</span><span class="sxs-lookup"><span data-stu-id="78d3c-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="78d3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78d3c-104">SYNTAX</span></span>

### <span data-ttu-id="78d3c-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="78d3c-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78d3c-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="78d3c-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d3c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="78d3c-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d3c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="78d3c-108">DESCRIPTION</span></span>
<span data-ttu-id="78d3c-109">Polecenie cmdlet Start-AzSqlElasticJob uruchamia zadanie zwracające nowe wykonanie zadania</span><span class="sxs-lookup"><span data-stu-id="78d3c-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="78d3c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78d3c-110">EXAMPLES</span></span>

### <span data-ttu-id="78d3c-111">Przykład 1 — Rozpoczynanie zadania zwracającego nowe wykonanie zadania</span><span class="sxs-lookup"><span data-stu-id="78d3c-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="78d3c-112">Rozpoczynanie zadania zwracającego nowe wykonanie zadania</span><span class="sxs-lookup"><span data-stu-id="78d3c-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="78d3c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78d3c-113">PARAMETERS</span></span>

### <span data-ttu-id="78d3c-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="78d3c-114">-AgentName</span></span>
<span data-ttu-id="78d3c-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="78d3c-115">The agent name</span></span>

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

### <span data-ttu-id="78d3c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78d3c-116">-AsJob</span></span>
<span data-ttu-id="78d3c-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="78d3c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78d3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d3c-118">-DefaultProfile</span></span>
<span data-ttu-id="78d3c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78d3c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78d3c-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="78d3c-120">-JobName</span></span>
<span data-ttu-id="78d3c-121">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="78d3c-121">The job name</span></span>

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

### <span data-ttu-id="78d3c-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="78d3c-122">-ParentObject</span></span>
<span data-ttu-id="78d3c-123">Obiekt zadania</span><span class="sxs-lookup"><span data-stu-id="78d3c-123">The job object</span></span>

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

### <span data-ttu-id="78d3c-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="78d3c-124">-ParentResourceId</span></span>
<span data-ttu-id="78d3c-125">Identyfikator zasobu zadania</span><span class="sxs-lookup"><span data-stu-id="78d3c-125">The job resource id</span></span>

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

### <span data-ttu-id="78d3c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d3c-126">-ResourceGroupName</span></span>
<span data-ttu-id="78d3c-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="78d3c-127">The resource group name</span></span>

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

### <span data-ttu-id="78d3c-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="78d3c-128">-ServerName</span></span>
<span data-ttu-id="78d3c-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="78d3c-129">The server name</span></span>

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

### <span data-ttu-id="78d3c-130">-Czekaj</span><span class="sxs-lookup"><span data-stu-id="78d3c-130">-Wait</span></span>
<span data-ttu-id="78d3c-131">Flaga oczekiwania wskazująca na zakończenie wykonywania zadania</span><span class="sxs-lookup"><span data-stu-id="78d3c-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="78d3c-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78d3c-132">-Confirm</span></span>
<span data-ttu-id="78d3c-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d3c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d3c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d3c-134">-WhatIf</span></span>
<span data-ttu-id="78d3c-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d3c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d3c-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78d3c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d3c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d3c-137">CommonParameters</span></span>
<span data-ttu-id="78d3c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d3c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d3c-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78d3c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d3c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78d3c-140">INPUTS</span></span>

### <span data-ttu-id="78d3c-141">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="78d3c-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="78d3c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78d3c-142">OUTPUTS</span></span>

### <span data-ttu-id="78d3c-143">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="78d3c-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="78d3c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78d3c-144">NOTES</span></span>

## <span data-ttu-id="78d3c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78d3c-145">RELATED LINKS</span></span>
