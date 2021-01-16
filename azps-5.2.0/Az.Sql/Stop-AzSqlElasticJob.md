---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325505"
---
# <span data-ttu-id="1a5ec-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="1a5ec-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="1a5ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1a5ec-103">Zatrzymuje zadanie o identyfikatorze wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="1a5ec-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="1a5ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a5ec-104">SYNTAX</span></span>

### <span data-ttu-id="1a5ec-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1a5ec-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a5ec-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="1a5ec-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a5ec-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1a5ec-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a5ec-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1a5ec-108">DESCRIPTION</span></span>
<span data-ttu-id="1a5ec-109">Polecenie cmdlet Stop-AzSqlElasticJob zatrzymuje zadanie z uruchomionym wykonaniem.</span><span class="sxs-lookup"><span data-stu-id="1a5ec-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="1a5ec-110">Zwraca bieżący stan wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="1a5ec-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="1a5ec-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a5ec-111">EXAMPLES</span></span>

### <span data-ttu-id="1a5ec-112">Przykład 1: zatrzymuje zadanie z uruchomionym wykonaniem zadania</span><span class="sxs-lookup"><span data-stu-id="1a5ec-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="1a5ec-113">Zatrzymuje uruchomione zadanie wykonania zadania i zwraca jego bieżący stan.</span><span class="sxs-lookup"><span data-stu-id="1a5ec-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="1a5ec-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1a5ec-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="1a5ec-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a5ec-115">PARAMETERS</span></span>

### <span data-ttu-id="1a5ec-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1a5ec-116">-AgentName</span></span>
<span data-ttu-id="1a5ec-117">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="1a5ec-117">The agent name</span></span>

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

### <span data-ttu-id="1a5ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a5ec-118">-DefaultProfile</span></span>
<span data-ttu-id="1a5ec-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a5ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a5ec-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="1a5ec-120">-JobExecutionId</span></span>
<span data-ttu-id="1a5ec-121">Identyfikator wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="1a5ec-121">The job execution id.</span></span>

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

### <span data-ttu-id="1a5ec-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="1a5ec-122">-JobName</span></span>
<span data-ttu-id="1a5ec-123">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="1a5ec-123">The job name</span></span>

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

### <span data-ttu-id="1a5ec-124">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="1a5ec-124">-ParentObject</span></span>
<span data-ttu-id="1a5ec-125">Obiekt bazy danych kontroli agenta</span><span class="sxs-lookup"><span data-stu-id="1a5ec-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="1a5ec-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1a5ec-126">-ParentResourceId</span></span>
<span data-ttu-id="1a5ec-127">Identyfikator zasobu wykonania zadania</span><span class="sxs-lookup"><span data-stu-id="1a5ec-127">The job execution resource id</span></span>

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

### <span data-ttu-id="1a5ec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a5ec-128">-ResourceGroupName</span></span>
<span data-ttu-id="1a5ec-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1a5ec-129">The resource group name</span></span>

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

### <span data-ttu-id="1a5ec-130">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="1a5ec-130">-ServerName</span></span>
<span data-ttu-id="1a5ec-131">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="1a5ec-131">The server name</span></span>

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

### <span data-ttu-id="1a5ec-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a5ec-132">-Confirm</span></span>
<span data-ttu-id="1a5ec-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a5ec-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a5ec-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a5ec-134">-WhatIf</span></span>
<span data-ttu-id="1a5ec-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a5ec-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a5ec-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1a5ec-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a5ec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a5ec-137">CommonParameters</span></span>
<span data-ttu-id="1a5ec-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a5ec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a5ec-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a5ec-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a5ec-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a5ec-140">INPUTS</span></span>

### <span data-ttu-id="1a5ec-141">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="1a5ec-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="1a5ec-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a5ec-142">OUTPUTS</span></span>

### <span data-ttu-id="1a5ec-143">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="1a5ec-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="1a5ec-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a5ec-144">NOTES</span></span>

## <span data-ttu-id="1a5ec-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a5ec-145">RELATED LINKS</span></span>
