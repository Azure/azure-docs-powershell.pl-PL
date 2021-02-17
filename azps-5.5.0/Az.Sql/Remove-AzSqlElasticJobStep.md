---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176826"
---
# <span data-ttu-id="f06f6-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="f06f6-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="f06f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f06f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f06f6-103">Usuwa etap zadania.</span><span class="sxs-lookup"><span data-stu-id="f06f6-103">Removes the job step</span></span>

## <span data-ttu-id="f06f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f06f6-104">SYNTAX</span></span>

### <span data-ttu-id="f06f6-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="f06f6-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f06f6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f06f6-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f06f6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f06f6-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f06f6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f06f6-108">DESCRIPTION</span></span>
<span data-ttu-id="f06f6-109">Polecenie Remove-AzSqlElasticJobStep cmdlet usuwa z zadania krok zadania</span><span class="sxs-lookup"><span data-stu-id="f06f6-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="f06f6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f06f6-110">EXAMPLES</span></span>

### <span data-ttu-id="f06f6-111">Przykład 1. Usuwanie kroku zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="f06f6-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="f06f6-112">Usuwanie kroku zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="f06f6-112">Removes a job step from a job</span></span>

### <span data-ttu-id="f06f6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f06f6-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="f06f6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f06f6-114">PARAMETERS</span></span>

### <span data-ttu-id="f06f6-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f06f6-115">-AgentName</span></span>
<span data-ttu-id="f06f6-116">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="f06f6-116">The agent name</span></span>

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

### <span data-ttu-id="f06f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f06f6-117">-DefaultProfile</span></span>
<span data-ttu-id="f06f6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f06f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f06f6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f06f6-119">-InputObject</span></span>
<span data-ttu-id="f06f6-120">Obiekt wprowadzania etapu zadania</span><span class="sxs-lookup"><span data-stu-id="f06f6-120">The job step input object</span></span>

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

### <span data-ttu-id="f06f6-121">— JobName</span><span class="sxs-lookup"><span data-stu-id="f06f6-121">-JobName</span></span>
<span data-ttu-id="f06f6-122">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="f06f6-122">The job name</span></span>

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

### <span data-ttu-id="f06f6-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f06f6-123">-Name</span></span>
<span data-ttu-id="f06f6-124">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="f06f6-124">The job step name</span></span>

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

### <span data-ttu-id="f06f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f06f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="f06f6-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f06f6-126">The resource group name</span></span>

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

### <span data-ttu-id="f06f6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f06f6-127">-ResourceId</span></span>
<span data-ttu-id="f06f6-128">Identyfikator zasobu kroku zadania</span><span class="sxs-lookup"><span data-stu-id="f06f6-128">The job step resource id</span></span>

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

### <span data-ttu-id="f06f6-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f06f6-129">-ServerName</span></span>
<span data-ttu-id="f06f6-130">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="f06f6-130">The server name</span></span>

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

### <span data-ttu-id="f06f6-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f06f6-131">-Confirm</span></span>
<span data-ttu-id="f06f6-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f06f6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f06f6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f06f6-133">-WhatIf</span></span>
<span data-ttu-id="f06f6-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f06f6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f06f6-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f06f6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f06f6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f06f6-136">CommonParameters</span></span>
<span data-ttu-id="f06f6-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f06f6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f06f6-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f06f6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f06f6-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f06f6-139">INPUTS</span></span>

### <span data-ttu-id="f06f6-140">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="f06f6-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="f06f6-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f06f6-141">OUTPUTS</span></span>

### <span data-ttu-id="f06f6-142">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="f06f6-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="f06f6-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f06f6-143">NOTES</span></span>

## <span data-ttu-id="f06f6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f06f6-144">RELATED LINKS</span></span>
