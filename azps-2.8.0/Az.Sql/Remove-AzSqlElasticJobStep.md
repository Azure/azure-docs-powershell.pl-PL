---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 83d5733144c07c229cf8b5321ee9d3417ab112ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887334"
---
# <span data-ttu-id="e7465-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="e7465-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="e7465-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7465-102">SYNOPSIS</span></span>
<span data-ttu-id="e7465-103">Usuwa krok zadania</span><span class="sxs-lookup"><span data-stu-id="e7465-103">Removes the job step</span></span>

## <span data-ttu-id="e7465-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7465-104">SYNTAX</span></span>

### <span data-ttu-id="e7465-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7465-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7465-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="e7465-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7465-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e7465-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7465-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e7465-108">DESCRIPTION</span></span>
<span data-ttu-id="e7465-109">Polecenie cmdlet Remove-AzSqlElasticJobStep usuwa etap zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="e7465-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="e7465-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7465-110">EXAMPLES</span></span>

### <span data-ttu-id="e7465-111">Przykład 1-usunięcie kroku zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="e7465-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="e7465-112">Usuwanie kroku zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="e7465-112">Removes a job step from a job</span></span>

## <span data-ttu-id="e7465-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7465-113">PARAMETERS</span></span>

### <span data-ttu-id="e7465-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e7465-114">-AgentName</span></span>
<span data-ttu-id="e7465-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="e7465-115">The agent name</span></span>

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

### <span data-ttu-id="e7465-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7465-116">-DefaultProfile</span></span>
<span data-ttu-id="e7465-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7465-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7465-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e7465-118">-InputObject</span></span>
<span data-ttu-id="e7465-119">Obiekt wejściowy kroku zadania</span><span class="sxs-lookup"><span data-stu-id="e7465-119">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7465-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="e7465-120">-JobName</span></span>
<span data-ttu-id="e7465-121">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="e7465-121">The job name</span></span>

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

### <span data-ttu-id="e7465-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7465-122">-Name</span></span>
<span data-ttu-id="e7465-123">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="e7465-123">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7465-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7465-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7465-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e7465-125">The resource group name</span></span>

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

### <span data-ttu-id="e7465-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7465-126">-ResourceId</span></span>
<span data-ttu-id="e7465-127">Identyfikator zasobu krok zadania</span><span class="sxs-lookup"><span data-stu-id="e7465-127">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7465-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e7465-128">-ServerName</span></span>
<span data-ttu-id="e7465-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="e7465-129">The server name</span></span>

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

### <span data-ttu-id="e7465-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7465-130">-Confirm</span></span>
<span data-ttu-id="e7465-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7465-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7465-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7465-132">-WhatIf</span></span>
<span data-ttu-id="e7465-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7465-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7465-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7465-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7465-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7465-135">CommonParameters</span></span>
<span data-ttu-id="e7465-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7465-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7465-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7465-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7465-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7465-138">INPUTS</span></span>

### <span data-ttu-id="e7465-139">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="e7465-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="e7465-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7465-140">OUTPUTS</span></span>

### <span data-ttu-id="e7465-141">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="e7465-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="e7465-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7465-142">NOTES</span></span>

## <span data-ttu-id="e7465-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7465-143">RELATED LINKS</span></span>
